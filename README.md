# Unified Revisions
This module provides a view of a content's complete revision history, including revisions for the node and it's preservation master and serivce files. The view can also be modified and serve as a template for other media fields. 
## Configuring the view for other types of media
The view shows revisions of media entities referenced to by the fields 'Preservation Master File' and 'Service File', to get revisions for media entities referenced by other fields, follow these steps:
1. Navigate to `/admin/structure/views/view/unified_revisions`
2. Under **Fields**, click *Add* and add select the desired media entity reference field, and click *Add and configure fields*
3. Check off *Exclude from display* and under **Formatter**, select *Entity ID*, then click *Apply*
4. Click *Add* under **Fields** again, select **View**, then click *Add and configure fields*
5. In the configuration menu, under **View** select *Media Revision Info* and keep **Display** set to *Defualt*
6. Expand the **REPLACEMENT PATTERNS** tab, locate the rendered replacement pattern for the field that was set up in steps 1-3 and paste it into the **Contextual filters** field
7. You can optionally add a label at this point to specify the media field being presented. Click *Apply* and *Save* the view
