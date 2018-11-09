
Audit Trail
==========================================

When something important happens in Chameleon – a batch is created or reassigned, a task is completed, a user's credentials are changed, etc. – an audit event is triggered and recorded.  Later, if you need to check what happened, when did it happen, and who caused it, you can refer to this audit trail and find out.

The audit trail is normally stored in database. The DB is configured using the standard OI_DB* vars. Events are stored in the audit_trail table. (If you don't have a DB set-up, then Chameleon will print the audit events to STDOUT and those will be recorded in whatever logfile the STDOUT is redirected to. If you don't have DB set up and could not be bothered to have STDOUT redirected to logfile, this is quite frankly your problem.)

Each audit event has the following information:

timestamp – when whatever happened happened;
event_id – what did actually happen; the event_id is a string like "batch_created", "user_removed", and so on;
trigger_id – who caused the thing to happen; in most cases this is a string like "user:alex", telling you who is responsible; sometimes this information is not available, so this field may be null;
event_data – more information about the event; this is a dictionary that tells you what changed; for example, if a new batch was just created, the event_data will have information about the batch ID, what tool it is, what is the title, etc.; if a batch was assigned to a user, the event_data will tell you which batch we are talking to and who is the user the batch was assigned to.
