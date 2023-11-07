This repository contains the assets required to produce the collection of icons used by the Ansible community.

## Icon Generator

The icon-making process works by fusing a CSV list of information with a base template to produce the final set of images. For this to work, you need to install the [Next Generator Inkscape extension](https://gitlab.com/Moini/nextgenerator) from Maren Hachmann.

It is also worth reading Máirín Duffy’s tutorials on this extension:
- How to automate graphics production with Inkscape // https://blog.linuxgrrl.com/2022/07/19/how-to-automate-graphics-production-with-inkscape/
- Part 2: How to automate graphics production with Inkscape // https://blog.linuxgrrl.com/2022/08/02/part-2-how-to-automate-graphics-production-with-inkscape/

### Workflow

When you need to create a new icon, follow these steps to update the CSV file using LibreOffice Calc:

- Download the desired icon from https://icon-sets.iconify.design/mdi/. 
- Make sure to save is in 350x350px SVG format and have the colour set to white.
- Save the icon in the 'images' folder. 
- Fill in the FileName as what you want the output file name to be in the CSV file. 
- For the CatColour, make sure it is the relevant colour code for the category of icon. 
  - '5cbec1' -> Top Level
  -	'102442' -> Ansible Working Groups
  -	'838991' -> Regional Rooms
  -	'f15b55' -> Ansible Conferences
  -	'000000' -> Neighbouring Projects
- For the Icon heading, fill in the file name of the svg you downloaded as is.
- Save the CSV file and open the "Template.svg" file in Inkscape.
- Navigate to Extensions > Export > NextGenerator…
- Ensure the following options are filled in correctly:
  - 'CSV file:' should point to the path of your CSV file with the data (e.g., '../Ansible-Icons/spreadsheet.csv').
  - 'Non-text values to replace:' should be set as `{"CatColour" : "000000" , "Icon" : "hand-wave-outline.svg"}`.
  - 'Number of sets in the template:' should be set to '1'.
  - 'File name pattern:' should be `%VAR_FileName%`.
  - 'Export file format:' should be 'PNG'.
  - 'DPI' should be set to '300'.
  - 'Save in:' should point to the location where you want the finalized cards to be saved (e.g., '../Ansible-Icons/generated-icons/').
- Click on the "Apply" button.

Once you've applied these steps, the completed icons will be available in the designated save location.

## Questions

[The forum](https://forum.ansible.com/c/project) is the best place to start discussions for a new icon or a change in the workflow. Ask away!

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md)

## Code of Conduct

The Ansible community team values diverse opinions and is committed to an inclusive
Please review and abide by our [CODE OF CONDUCT](CODE_OF_CONDUCT.md).

## License

[![License: CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/4.0/80x15.png)](https://creativecommons.org/licenses/by-sa/4.0/)

## Thank you

Ansible depends on community involvement - thank you for being a part of it!
