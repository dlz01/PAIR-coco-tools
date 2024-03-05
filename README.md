# coco_tools

This repository contains two Jupyter notebooks: `merge_coco.ipynb` and `xml2coco.ipynb`. These notebooks are designed for processing and combining datasets in the COCO format, as well as converting datasets from XML (PASCAL VOC) format to COCO format. The tools provided are specifically useful for agricultural research, such as weed detection in crop fields, but can be adapted for various object detection tasks.

## `merge_coco.ipynb`

This notebook provides a comprehensive suite of functions for merging multiple COCO datasets into a single, unified dataset. Key functionalities include:

- **Copying JSON files**: Allows for copying annotation files from source to target directories.
- **Filtering datasets by category**: Facilitates copying only those datasets that contain specific categories, as specified in a detection file.
- **Cleaning up categories**: Enables the removal of unused categories from annotation files to streamline the dataset.
- **ID management**: Supports the reassignment of category and annotation IDs to ensure consistency across merged datasets.
- **Combining datasets**: A core function to combine two COCO annotated files into a single output file, handling overlaps in image and annotation IDs.
- **Image file management**: Includes moving and copying image files associated with the JSON annotations to the combined dataset directory.

## `xml2coco.ipynb`

This notebook is designed to convert XML annotation files (specifically in PASCAL VOC format) into the COCO format. Its functionalities include:

- **Copying image and XML files**: Transfers image files and relevant XML annotation files into a target directory for processing.
- **XML to COCO conversion**: Parses XML files to extract annotations, images, and category information, organizing them into the COCO format.
- **Annotation refinement**: Post-conversion, it can clean image filenames within the COCO JSON to ensure they follow a consistent format.

## Usage

To use these tools, follow the step-by-step instructions within each notebook. Make sure to adjust paths and filenames according to your dataset structure. Both notebooks are designed to be modular, allowing users to execute only the necessary steps for their specific task.

### Requirements

These notebooks require Python 3 and the following libraries: `tqdm`, `shutil`, `json`, `pathlib`, and `os`. For XML to COCO conversion, `xml.etree.ElementTree` and `glob` are also needed.

## Credits

- `merge_coco.ipynb` is adapted from contributions by [mohamadmansourX/Merge_COCO_FILES](https://github.com/mohamadmansourX/Merge_COCO_FILES).
- `xml2coco.ipynb` utilizes code from [CivilNet/Gemfield](https://github.com/CivilNet/Gemfield) for XML parsing and COCO JSON construction.
