# Unified Revisions
This module provides a view of a content's complete revision history, including revisions for the node and its [Islandora Content Type](https://github.com/digitalutsc/islandora_content_type) media fields (preservation master file and service file). The view can also be modified and serve as a template for other media fields. 
Unified Revisions generates the final view by layering together seperate 5 views using the [Views Field View](https://www.drupal.org/project/views_field_view) drupal module.
<p align="center">
   <img width="398" alt="Screen Shot 2021-11-03 at 1 07 24 PM" src="https://user-images.githubusercontent.com/62853290/140138040-d5648573-b2d0-4484-89fb-6c4bab88d513.png">
</p>


## Configuring the view for other types of media
The view shows revisions of media entities referenced to by the [Islandora Content Type](https://github.com/digitalutsc/islandora_content_type) fields 'Preservation Master File' and 'Service File', to get revisions for media entities referenced by other fields, follow these steps:
1. Navigate to `/admin/structure/views/view/unified_revisions`
2. Under **Fields**, click *Add* and add select the desired media entity reference field, and click *Add and configure fields*
3. Check off *Exclude from display* and under **Formatter**, select *Entity ID*, then click *Apply*
4. Click *Add* under **Fields** again, select **View**, then click *Add and configure fields*
5. In the configuration menu, under **View** select *Media Revision Info* and keep **Display** set to *Defualt*
6. Expand the **REPLACEMENT PATTERNS** tab, locate the rendered replacement pattern for the field that was set up in steps 1-3 and paste it into the **Contextual filters** field
7. You can optionally add a label at this point to specify the media field being presented. Click *Apply* and *Save* the view
