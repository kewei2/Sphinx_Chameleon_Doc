
Release History
==========================================

Chameleon Releases
PENDING CHANGES (Test Chameleon only, sometimes in Dev):
<none>
Chameleon 7.16.0, released on Nov 9, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Updates in the Image Stack tool:
If the session expires before a user completes a task, the user will be asked to login again and can continue work without losing any data. See PT-690. 
In Polygons mode: Resolving inconsistencies in the polygon data (the data_fields). See PT-702.
New REST API action, 'get_user', to retrieve detailed information about a Chameleon user.
Updated Image Stack sample batch to show where to keep metadata about the whole batch and about each task. See PT-698.
Chameleon 7.15.0, released on Oct 31, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Ability of regular workers to review batches, provided the worker is explicitly assigned as a reviewer to the given batch. See PT-693.
Minor updates in the landing page (batch list). 
Bugfix: Do not warn when navigating away from tasks in peek mode. See PT-692.
Chameleon 7.14.0, released on Oct 23, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Adding shortcut keys in review mode for Object Marking tool. See PT-688.
Switched the SSL configuration from command-line options to environmental vars. See the SSL_* env vars in the Running Chameleon section.
Bugfix: The Campaigns selector was not displaying correctly in certain versions of FireFox.
Chameleon 7.13.1, released on Oct 23, 2018. Requires OFL 24.16.3 & Services 4.21.0:
With Redis back-end, switching to server-side session management to make sure sessions are invalidated on logout. See PT-686.
Setting the secure flag on the session cookie (when SSL is enabled). See PT-687.
Chameleon 7.13.0, released on Oct 22, 2018. Requires OFL 24.16.3 & Services 4.21.0:
HTTPS support when Chameleon is run directly as a Flask application. See Running Chameleon.
Image Stack tool: Warn if navigating away from the page. See PT-679.
Chameleon 7.12.2, released on Oct 17, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Bugfix: Error message on the Batches page when session expires is gone, instead browser now redirects to the login page. See PT-677.
Bugfix: Image Stack tool / Polygons mode: The data query shortcut (?) is now available only when there is polygon data; shortcut was also not showing in the help. See PT-678.
Bugfix: Resolved issue where duplicated directories were created in the batch data directory. See PT-682.
Chameleon 7.12.1, released on Oct 15, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Better performance on the Batches page. See PT-676. 
Improved and simplified batch list page for regular workers.
Chameleon 7.12.0, released on Oct 15, 2018. Requires OFL 24.16.3 & Services 4.21.0:
New main page (Batches) – visually the page is the same, but it is faster to support the increased number of registered batches. See PT-626.
Invalidating login session after a period of inactivity. See the note on the SESSION_TIMEOUT var in the Environment Variables section, and PT-120.
Chameleon 7.11.1, released on Oct 3, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Bugfix: Image Stack tool: The Shift + drag pan shortcut was interfering with the shortcut for drawing straight lines in Paint mode; pan is now Alt + drag; zoom is Alt + Shift + drag.
Chameleon 7.11.0, released on Oct 3, 2018. Requires OFL 24.16.3 & Services 4.21.0:
The Tree Picker widget has search + recent selections. See PT-661.
Image Stack tool updates:
New validations for crossing, self-intersecting, and overlapping polygons. See PT-565. 
Shift + drag pans the image and Alt + drag zooms in and out. NOTE: Those shortcuts have been changed in the next version! See PT-665.
Adjustable line width in Polygon marking mode. See PT-667.
Extra validations for custom forms – in every place in Chameleon when a custom form is generated, we make sure each of the data fields has a name and that all field names in a form are unique.
Bugfix in the Tree Picker – the data recorded in the task result JSON was the tree node label instead of the value.
Add list_campaigns API.
Chameleon 7.10.0, released on Sep 28, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Image Stack tool:
The estimated number of tasks available to a given worker is shown on the task page. Note that if multiple workers are working on same batch and are competing for the same tasks, the number may for one worker may change unexpectedly and go down as soon as other workers complete tasks. See PT-30.
In Polygon marking mode, the metadata form becomes visible as soon as the worker starts editing a polygon, making it easier to enter polygon data.
Larger popup for the Tree Picker widget to make handling of deeper hierarchies easier. See PT-660.
The Repository Browser UI is deprecated.
Bugfix: SVG images returned with the wrong content type in some cases. See Chameleon PR 207.
Chameleon 7.9.1, released on Sep 27, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Bugfix: The supervisor's Batches page search was not working correctly. See PT-659.
Chameleon 7.9.0, released on Sep 26, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Multiple batches can be published simultaneously. See PT-199. 
Support for configurable task timeout. See PT-654.
Distinct custom cursor when removing polygons in the Image Stack tool. See PT-648.
Bugfixes:
Batch CSV export does not handle correctly special characters in the campaign ID. See PT-656.
Page redirect does not work after publishing a batch. See PT-644.
Chameleon 7.8.0, released on Sep 24, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Converting the supervisors' Batches page to the new by-campaign style. See PT-570.
Adding a Tree Picker widget, available in all tools that use custom forms. See PT-622.
Image Stack tool:
In Polygon marking mode, ability to associate custom forms with each polygon. See PT-645.
Ability to open images on a separate tab, using a link in the task instructions. See PT-631.
Shortcut for fitting image to window. See PT-621.
Bugfixes:
Annotation screenshot sometimes does not get updated. See PT-627 & PT-628.
The level selector widget in the Image Stack tool did not work in FireFox. See PT-649.
Error when registering a batch with a .tar.gz extension. See PT-620.
Chameleon 7.7.0, released on Sep 13, 2018. Requires OFL 24.16.3 & Services 4.21.0:
After registering a batch, the Campaign selector is set to the campaign of the newly registered batch and the Search field is cleared, ensuring that the new batch is visible.  See PT-612.
Adding several demo batches in the samples/batches/demo/ directory. See PT-601.
HTML of superuser home page optimized to slightly reduce loading time. See PT-624.
Bugfixes:
Invalid catch syntax in JS code causing issues on some browsers.  See PT-614.
Registering a completed batch from the API was not possible. Workaround was to register those through the UI.
Chameleon 7.6.0, released on Sep 5, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Tank Marking tool: Keep position when a new tank mark is selected. See PT-595.
Minor improvements in handling of a couple of errors. See PT-525.
Fixed a bug when showing task UI in AOI Change Tool. See PT-611.
Chameleon 7.5.0, released on Aug 23, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Support for radio-button shortcuts in the Image Stack tool. See PT-582 and PT-593.
Add Chameleon API to pass/fail task. See PT-597.
Chameleon 7.4.0, released on Aug 21, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Changing logic for setting step-size in tank fill marking tool. See PT-596.
Making FINE_EXTERNAL_DIAMETER_ADJUSTMENT, FINE_HEIGHT_ADJUSTMENT in tank marking tool configurable. See PT-512.
Reversing the display order in the supervisor and regular user batch list – newest batches are at the top. See PT-360.
Bugfix: If worker cleaned all points in the Image Stack tool (categorized points marking mode) using the Q shortcut, points marked on this particular task in the future were not persisted.
Chameleon 7.3.0, released on Aug 9, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Image Stack tool updates:
Ability to mark bounding boxes. See PT-566.
More validations. See PT-579.
Bugfix: When selecting a range of batches from the admin page, batches that are not visible may get selected. See PT-586.
Chameleon 7.2.0, released on Aug 8, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Better accuracy of the displayed point position in Points and Categorized Points modes. See PT-585.
The new "by-campaign" superuser main page is now taken out of experimental mode; the old page is deprecated.
Chameleon 7.1.0, released on Aug 7, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Superusers can now 'peek' at batch tasks in any order, without completing them. See PT-573.
Ability to download information and statistics about all batches as CSV. See PT-578.
Image Stack tool / Polygons mode:
Ability to move polygons from one category to another. See PT-202.
Polygon validation. See PT-575.
No more error messages in the browser console when opening a task that does not have annotated screenshot. See PT-561.
Minor bugfixes and usability improvements in the admin Batches page.
Chameleon 7.0.0, released on Aug 1, 2018. Requires OFL 24.16.3 & Services 4.21.0:
Campaign management is now mainstream: 
Campaign is mandatory for newly deployed batches on all Chameleon servers.
Batches are grouped by campaign in the admin UI for all Chameleon servers.
Chameleon 6.3.2 HF1, released on Jul 26, 2018. Requires OFL 24.12.0 & Services 4.14.0:
Bugfix: Annotation screenshot gallery was broken in the previous version (PT-560).
Bugfix: Sequential ordering in the Multi-Image Classification tool was not working.
Chameleon 6.3.1, released on Jul 26, 2018. Requires OFL 24.12.0 & Services 4.14.0:
Bugfix: If worker cleaned all polygons in the Image Stack tool (polygon marking mode) using the Q shortcut, polygons marked on this particular task in the future were not persisted.
Chameleon 6.3.0, released on Jul 25, 2018. Requires OFL 24.12.0 & Services 4.14.0:
Requiring valid campaign ID for new batches; the requirement applies only to the Test Chameleon server; Dev and Prod servers are exempt until Aug 1 (PT-536).
New batches page – grouping by campaign, search more prominent; enabled only in experimental mode (PT-547).
Adding border around letters in the annotation screenshots to make text easier to read (PT-551).
OFL / Services version upgrade (PT-543).
Chameleon 6.2.0, released on Jul 17, 2018. Requires OFL-23.12.2 & Services 4.2.0:
Image Stack tool updates:
Multipolygon mode: Ability to duplicate polygons (PT-541).
Error message in JS console if the tool IDs in tasks.json do not match the IDs as defined in batch.json (PT-542).
Support for multiple batch upload (PT-24).
Ability to remove annotation screenshots (PT-534).
Dev Chameleon is now switched to the Dual tile service. 
Chameleon 6.1.1, released on Jul 11, 2018. Requires OFL-23.12.2 & Services 4.2.0:
Bugfix: Exceptions in the get_batches() REST API method.
Chameleon 6.1.0, released on Jul 10, 2018. Requires OFL-23.12.2 & Services 4.2.0:
All annotated screenshots for a batch can be viewed on a single page (PT-527).
Bugfix: Discrepancies in the results returned by the get_batches() REST API method (PT-529).
Chameleon 6.0.0, released on Jul 9, 2018. Requires OFL-23.12.2 & Services 4.2.0:
Ability to attach annotated screenshots to tasks. Currently supported only in the Image Stack tool (PT-518).
Chameleon 5.9.1, released on Jun 29, 2018. Requires OFL-23.12.2 & Services 4.2.0:
Keyboard shortcuts for quick task review. See PT-203.
Unifying the task status strings – we used to have cancelled and canceled, now we've switched entirely to the US spelling (single l).
Bugfix: Images were not showing up sometimes in the Image Stack tool.
Chameleon 5.9.0, released on Jun 28, 2018. Requires OFL-23.12.2 & Services 4.2.0:
Image Stack tool updates:
Optional widget for displaying the name of the top image overlay (PT-513).
Ability to automatically set zoom level to fit images to task window (PT-387).
Switching to the Dual tile service, making integration testing easier (PT-517).
Improved performance with DB back-end (PT-516).
Chameleon 5.8.0, released on Jun 18, 2018. Requires OFL-23.12.2 & Services 4.2.0:
Adding a UI for reassign_tasks API (PT-510).
Image Stack tool: Ability to set default visibility of image overlays (PT-511).
Chameleon 5.7.1, released on Jun 8, 2018. Requires OFL-23.12.2 & Services 4.2.0:
Tank Marking Tool: Reduce Default Step Size and make it configurable (PT-512).
Adding a reassign_tasks api (PT-510).
Chameleon 5.7.0, released on May 29, 2018. Requires OFL-23.12.2 & Services 4.2.0:
Image Stack Tool: Support for image overlays (PT-176).
Chameleon 5.6.0, released on May 24, 2018. Requires OFL-23.12.2 & Services 4.2.0:
Image Stack Tool: Ability to configure point size in points and categorized points modes (PT-453).
Adding a get_batches method to the REST API (PT-492).
Abolishing the tyranny of top-folder enforcement when publishing batches.
Plugging up a memory leak in uWSGI (PT-497).
Bugfix: Occasional exception when publishing batches.
Chameleon 5.5.0, released on May 17, 2018. Requires OFL-23.8.6 & Services 3.12.0:
Adding a list_users method to the REST API (PT-490).
Bugfix: Occasional exceptions when polygons are cleared in the Image Stack tool (PT-493).
Chameleon 5.4.0, released on May 15, 2018. Requires OFL-23.8.6 & Services 3.12.0:
Chameleon service client. 
Adding a delete_batch method to the REST API.
Audit log event changes: Logging the username for API-triggered events, logging batch_published event in api_publish, more detailed batch_modified events, a couple of minor bugfixes.
Improved performance when requesting tiled imagery that lines up with tile boundaries (PT-470).
Supervisors are not able to see all batches anymore, just batches that are assigned to them as workers or reviewers, or batches that are available to everybody to work on (PT-468).
Ability to go to batch tasks straight from the Batch Info page (PT-401).
Bugfix: Occasional errors (502) on the batch list page shortly after a bunch of batches are published (PT-488).
Chameleon 5.3.0, released on May 3, 2018. Requires OFL-23.8.6 & Services 3.12.0:
Minor simplification in the REST API parameters of the batch assign action – input is a single dictionary, instead of a list of dictionaries; code calling the REST API directly may need to be updated.
Worker ID is now always present in the task_result_modified audit log events to make it easier to track work quality (PT-184).
Updates and bugfixes in the startup script, related to the DB audit trail logger, adding more debug messages (PT-467).
More sample batches.
Chameleon 5.2.0, released on Apr 25, 2018. Requires OFL-23.8.6 & Services 3.12.0:
Forms used in the Image Stack, AOI Data, and Tank Marking tools: ability to display a choice set as a set of radio buttons, in addition to a combo box (PT-447).
Resolved an exception when removing all completed results from a batch (PT-452).
Chameleon 5.1.0, released on Apr 24, 2018. Requires OFL-23.8.6 & Services 3.12.0:
Exceptions are propagated to UI – this helps resolve runtime issues (PT-445).
Bugfix: User ID was missing from the USER_MODIFIED audit log events (PT-439).
Bugfix: A bad batch could cause the Chameon admin homepage to fail (PT-445).
Image Stack tool / polygon mode: Ability to blink static marks independently of marked polygons (PT-442).
Chameleon 5.0.0, released on Apr 20, 2018. Requires OFL-23.8.6 & Services 3.12.0:
Chameleon now has audit log with data about what happened, when did it happen, and who caused it to happen (PT-184). 
DB repository back-end available (PT-375).
Improvements in the batch repository, when running with DB back-end.
Script for migration from Redis- to DB-backend – bin/migrate_to_db_store.py (PT-340).
Bugfix: If the value of a custom display field in the Batch Info page was float or integer, the page crashed.
Chameleon 4.3.0, released on Mar 23, 2018. Requires OFL-21.8.4 & Services 2.21.0:
Map Marking tool: Ability to blink static marks (PT-406).
Chameleon 4.2.0, released on Mar 22, 2018. Requires OFL-21.8.4 & Services 2.21.0:
Map Marking tool: Ability to transfer marked points/polygons between subsequent tasks (PT-400).
Chameleon 4.1.0, released on Mar 16, 2018. Requires OFL-21.8.4 & Services 2.21.0:
Better error messages on task pages (PT-374).
Image Stack tool / Positioning mode: Added positioning constraints (PT-376).
Image Classification tool suports center mark.
Chameleon 4.0.0, released on Feb 28, 2018. Requires OFL-21.8.4 & Services 2.21.0:
Chameleon supports Postgres as backend; default is still Redis (PT-337). 
The REST API now supports batch worker/reviewer assignment (PT-357).
Image Stack tool updates:
support for transfer of information between tasks (PT-309, PT-331);
in Polygon mode, ability to drag polygons (PT-373).
Better error messages when there is a problem registering a batch (PT-367).
Chameleon 3.11.0, released on Feb 22, 2018. Requires OFL-21.8.4 & Services 2.21.0:
Updates in the Image Stack tool / Polygon mode:
configurable line width of the polygons marked by the user (PT-350);
allow classification changes without closing the active polygon (PT-364);
allow dragging points from the active (not yet complete) polygon (PT-365);
changing zoom levels, images, or tools does not close the currently open polygon (PT-366).
Chameleon 3.10.0, released on Feb 21, 2018. Requires OFL-21.8.4 & Services 2.21.0:
The AOI Change tool and the Tank Marking tool now support imagery from the new Tile Service (PT-348, PT-349).
Chameleon 3.9.0, released on Feb 20, 2018. Requires OFL-20.3.0 & Services 2.15.0:
Introducing "Light" mode, where non-essential functionality is disabled (PT-345).
The Image Stack tool now transfers zoom level between tasks and supports zoom level configuraiton per batch/task (PT-346).
Chameleon 3.8.1, released on Feb 17, 2018. Requires OFL-20.3.0 & Services 2.15.0:
Bugfix: The 'scale' argument was not working in the 'tiled_region' service for new tile service imagery (PT-344).
Chameleon 3.8.0, released on Feb 15, 2018. Requires OFL-20.3.0 & Services 2.15.0:
Image Stack tool now has Positions mode for marking the locations of a set of predefined objects (PT-339).
Chameleon 3.7.1, released on Feb 13, 2018. Requires OFL-20.3.0 & Services 2.15.0:
Minor bugfixes in the Image Stack tool – active category in Polygons and Categorized Points modes get reset when zoom level is changed, or when another image is selected.
Chameleon 3.7.0, released on Feb 13, 2018. Requires OFL-20.3.0 & Services 2.15.0:
Image Stack Tool updates:
adding polygon-marking mode (PT-313);
support for static (read-only) marks on images (PT-319, PT-338);
minor bugfixes.
Stopped using Carbon for logging (PT-244).
Chameleon 3.6.0, released on Feb 2, 2018. Requires OFL-20.3.0 & Services 2.15.0: 
Updates to the Image Stack tool - added the Categorized Points mode (PT-308). 
Bugfix: Chameleon batch API: call for retrieving batch JSON only does not work (PT-305).
Chameleon 3.5.1, released on Jan 9, 2018. Requires OFL-19.1.1 & Services 2.12.0:
Bugfix: Resolving an issue with new Tile Service imagery on Prod (PT-285).
 Chameleon 3.5.0, released on Jan 9, 2018. Requires OFL-19.0.0 & Services 2.12.0:
Image Stack Tool now supports tiled imagery (PT-283).
Copyright statements added in code (PT-278).
Chameleon 3.4.1, released on Jan 3, 2018. Requires OFL-18.4.0 & Services 2.7.0:
The Batch Info page was returning a 500 error if the custom columns were not configured correctly (PT-277).
Chameleon 3.4.0, released on Dec 21, 2017. Requires OFL-18.4.0 & Services 2.7.0:
Extending the REST API with two new actions (PT-264, see the REST API section for details):
list_batches, returning all batches currently registered on Chameleon, and
get_batch_stats, returning detailed information about a particular batch.
Chameleon 3.3.0, released on Dec 18, 2017. Requires OFL-18.4.0 & Services 2.7.0:
REST API for registering, downloading, and publishing batches; see the REST API section (PT-223).
Enhancements in the batch_util.py script (PT-249).
Chameleon 3.2.0, released on Nov 29, 2017. Requires OFL-16.0.1 & Services 2.0.1:
Ability to specify the order in which tasks will be presented to the worker and to the reviewer (PT-241).
Ability to review tasks by groups, depending on a task/result property (PT-194).
Chameleon 3.1.0, released on Nov 28, 2017. Requires OFL-16.0.1 & Services 2.0.1:
The Map Marking tool now supports overlay imagery delivered from the new tile service.
Added a command-line tool, bin/polygon_scene_overlay.py, to generate scene-overlay map marking batches (OFL-2323).
Ability to customize the fields in the Batch Info page (PT-205, PT-206).
Chameleon 3.0.0, released on Oct 24, 2017. Requires OFL-16.0.1 & Services 2.0.1:
Switched Chameleon to the new service packages.
Added the supervisor user category (PT-227).
Chameleon 2.12.0, released on Sep 26, 2017. Requires OFL-14.1.2:
REST endpoints for getting tiles and tiled regions from the new Tile Service (see the REST Services section above); endpoint supports on-the-fly band manupulation (PT-191).
Map Marking tool now supports attachment (RSF-2911).
Chameleon 2.11.1, released on Sep 19, 2017. Requires OFL-13.8.2:
Some work to resolve (or at least – identify the cause for) a problem where a shceduled batch does not always get removed from the S3 repo when published.
Chameleon 2.11.0, released on Sep 14, 2017. Requires OFL-13.8.2:
Strict validation of the working batch directory to avoid losing information (PT-178).
Chameleon 2.10.1, released on Sep 12, 2017. Requires OFL-13.8.2:
Updated startup scripts – batch data directory was pointing to the in-docker /data folder, instead of the shared EFS data folder.
Chameleon 2.10.0, released on Sep 5, 2017. Requires OFL-13.8.2:
Map Marking tool: Classification choices can be changed during task review (OFL-2141).
Chameleon 2.9.0, released on Aug 17, 2017. Requires OFL-13.6.0: 
Image Stack tool: Resolving an issue where unnecessary images and data were saved with completed batches (OFL-1884).
Adding a batch action Remove all results to remove all work performed on a batch (OFL-1921).
Map Marking tool: Ability to blink all marks (OFL-2061).
Chameleon 2.8.0.1 (hotfix), released on Aug 3, 2017. Requires OFL-13.6.0:
Tank Marking tool: Fixing wrong external shadow diameter adjustment during task review (OILINV-2633).
Chameleon 2.8.0, released on July 28, 2017. Requires OFL-13.6.0:
Tank Marking tool: Adding a scene-selector mode, allowing the worker to select the most appropriate scene to mark (OILINV-2532).
Batch review page: Making it easier to identify which task each result belongs to by drawing borders around each cell in the task review status table and adding result index next to each worker name.
Chameleon 2.7.1, released on July 21, 2017. Requires OFL-13.6.0:
Minor fix in the Map Marking tool – the Notes text area was too wide and was not fully visible.
Chameleon 2.7.0, released on July 14, 2017. Requires OFL-13.6.0:
Ability to change the batch repeat count from the UI. Click on batch statistics link (% Completed/Reviewed/Passed) to open batch info page, then click on the Change number of repeats action link (OFL-1655).
Fixing oversaturated areas when pansharpening overexposed images (OFL-1871).
When using polygon mode in the Image Marking tool, the node selecting distance (in screen pixels) was changing based on the zoom factor, making it difficult to work with the tool at hight zoom levels. (OFL-1895).
Chameleon 2.6.0, released on July 6, 2017. Requires OFL-13.6.0:
Image Stack Tool: If the task has a large number of images, the image selector menu at the top of the task UI can now span multiple rows.
Image Marking Tool:
In local imagery mode, a link to Google Maps will be shown if the image file name is a proper tile ID (OFL-1806).
The tool now ignores hidden files (file names starting with dot) when creating tasks from images; MacOS has the nasty habit of creating .-files without asking...
Fixing keyboard shortcuts (OFL-1833).
Chameleon 2.5.0, released on Jun 19, 2017. Requires OFL-13.6.0:
Tiled region imagery (see the REST Services section above) can be pansharpened on the fly by requesting band 92. If there is Pan and RGB image, those will be combined in a pansharpened image on the fly, otherwise Pan or RGB will be returned, whichever is available (OFL-1658).
Image Stack tool enhancement to allow different tools to be available for different images in a task (OFL-1760).
Chameleon 2.4.0, released on Jun 6, 2017. Requires OFL-13.4.6:
Ability to designate regular (non-superuser) workers as reviewers (OFL-1692).
Tank Marking tool:
Resolving a backward compatibility issue (OFL-1594).
Better visibility for the markings and toggle marking visibility (OFL-1620).
Support for independent marking of the tank external shadow (OFL-1643).
Default tank fill ratio is now 1.0 (used to be 0.5). This simplifies the initial tank dimensioning.
Chameleon 2.3.0, released on May 18, 2017. Requires OFL-12.5.2:
Multiple batch download from the batch repository (OFL-258).
Tank Marking tool bugfixes: Tool not working in Tank Outline mode; markings not visible on task review and rework (OFL-1543).
Minor UI / CSS fixes.
Chameleon 2.2.1, released on May 9, 2017. Requires OFL-12.5.2:
The instructions in the Image Stack tool can be parametrized on per-task basis (OFL-1512).
Brighter and bigger marks in the multipoint marking utility of the Image Stack tool (OFL-1506).
Chameleon 2.2.0, released on Apr 18, 2017. Requires OFL-12.5.2:
New Image Stack tool for various marking tasks over a stack of images (OFL-1345).
Bugfix: Resolving a caching issue in the Image Marking tool (OFL-1425).
Chameleon 2.1.0, released on Apr 7, 2017. Requires OFL-12.3.0:
New AOI Data Tool for entering/correcting marked objects metadata (OILINV-694).
Tank Marking tool updates: ability to directly enter and view tank dimensions, support for metadata fields (OILINV-639).
Shortcut for deleting a complete polygon in the Map Marking tool (RSF-2216).
Chameleon 2.0.3, released on Mar 23, 2017. Requires OFL-11.1.2:
Clicking on "Chameleon" in the menu bar will show popup with the Chameleon version (OFL-1271).
Bugfix: Passing a task will clear the "classification" attribute in the Object Marking tool (OFL-1312).
Chameleon 2.0.2, released on Mar 20, 2017. Requires OFL-11.1.2:
AOI Marking tool: allow editing during task review (OFL-1267).
Chameleon 2.0.1, released on Mar 17, 2017. Requires OFL-11.1.1.
Bugfixes in the Point Marking tool – the review UI was not working properly. 
Adding a sun position indicator REST API call.
Adding sun position indicator in the Point Marking and Image Classification tools (OFL-1239).
The original Chameleon favicon is back by popular demand!
Object Marking tool – keeping accurate marking positions after zoom changes (OFL-1265).
Chameleon 2.0.0 released on Mar 6, 2017. Requires OFL-11.0.7.
Chameleon facelift – making the UI slightly less nasty (OFL-1207).
Choice between sliders and checkboxes for control of overlay opacity in the Map Marking tool (OFL-1217).
Corrected order of image overlays – the first overlay in the list is on the top.
Chameleon 1.4.2 released on Feb 24, 2017. Requires OFL-11.0.0.
Command-line tool for creating and processing generic Map Marking batches – bin/map_marking.py (OFL-714).
Ability to download only the JSON for a batch (OFL-1206).
Chameleon 1.4.1 released on Feb 9, 2017. Requires OFL-11.0.0.
Changes to Ops script (config.sh) to handle the new location of the OFL source files (OFL/src/py).
Chameleon 1.4.0 released on Jan 20, 2017. Requires OFL-10.1.4.
All (most?) tools should support redeployment of [partially] completed batches to different Chameleon server without losing the task results (OFL-1096).
Adding scale parameter in the Tank Marking tool.
Multi-Image Classification tool.
Support for non-georeferenced image overlays in the Map Marking tool (JPEG, PNG).
Support for tiled region imagery in the Image Classification tool.
Chameleon 1.3.0 released on Jan 3, 2017. Requires OFL-9.2.0.
Adding support for scale parameter of the get_region REST call.
Various minor tool UI updates.
Chameleon 1.2.0 released on Dec 6, 2016. Requires OFL-8.1.0.
Minor changes and tool upgrades.
Chameleon 1.1.0 released on Nov 30, 2016. Requires OFL-8.1.0.
Migration to a more recent OFL version. 
Chameleon 1.0.0 released on Nov 18, 2016. Requires OFL-4.0.2.
Chameleon Client Releases
PENDING CHANGES (not released, based on Chameleon 7.16.0+, OFL 25.2.0+, and Services 4.48.0+):
Updates in the Chameleon CLI. Tool is now renamed chameleon from batch_util.py and has a number of changes in commands and output data.
Adding new method, get_user(), to retrieve detailed information about a user.
Chameleon Client 1.3.0, released on Oct 29, 2018. Based on Chameleon 7.14.0+, OFL-23.12.2, and Services 4.2.0:
New command-line Chameleon tool. See batch_util.py and PT-258.
Ability to skip SSL certificate validation by setting the DO_NOT_VERIFY_SSL_CERT environment variable to False. See PT-691.
Fixed the docstring for the get_batches() method.
Chameleon Client 1.2.0, released on Aug 13, 2018. Based on Chameleon 7.3.0+, OFL-23.12.2, and Services 4.2.0:
Minor bugfixes.
Unit tests.
Chameleon Client 1.1.0, released on Jul 2, 2018. Based on Chameleon 5.9.1+, OFL-23.12.2, and Services 4.2.0:
Chameleon geometry utility library, chameleon_client.util.geomutil (PT-320).
Chameleon Client 1.0.0, released on May 24, 2018. Based on Chameleon 5.6.0+, OFL-23.12.2, and Services 4.2.0:
Initial release.

