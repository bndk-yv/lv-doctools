# lv-doctools

Utility to include LabVIEW screenshots in Markdown: easily reference your VIs, controls and classes by their path in the project.

### Usage:

1. Place [DocTools.lvlibp](../doc/DocTools.lvlibp) in your documentation folder (first level subfolder of project directory)
2. Open the library and run Gather Images.vi
3. An additional folder "img" is created in the documentation directory, containing screenshots of all .vi, .ctl and .lvclass files in the project directory.


Specific screenshots can be referenced as:

| Source Directory | FP Image  | BD Image |
|-|-|-|
| /\_dummy\_/folder1/folder2/dummy4.vi | /doc/img/\_dummy\_/folder1/folder2/dummy4.vi_FP.png |  /doc/img/\_dummy\_/folder1/folder2/dummy4.vi.png |
| /\_dummy\_/folder1/dummy2.ctl |  /doc/img/\_dummy\_/folder1/dummy2.ctl.png | - |
| /\_dummy\_/folder1/folder2/dummy3.lvclass |  /doc/img/\_dummy\_/folder1/folder2/dummy3.lvclass.png | - |

### Planned features:

- Check whether specific image appears in any .md files in the project directory. Option: save all images or only save/update images that are actually referred to in .md files.
- Export baked-in VI & control documentation as HTML

TODO: Right now the extensions are not as they should be! str(file+ext+additional_ext)
