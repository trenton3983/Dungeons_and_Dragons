# Dungeons & Dragons

- D&D spells below 5th edition
- I'm creating a `spells.json` file, with `list` of `dicts`, for spells from the 2nd edition spell compendiums.
 - Spells not contained in those volumes will be added later
- Feel free to contribute, just follow the format in the JSON file
- The project is out of personal love of D&D.  Being a habitual caster, I want a magical method to quickly bring a spell or group of spells to my fingertips, without the need to reference a dusty tome or carry 50 lbs or resources.
 - Sometimes I play 5th edition, which has great digital resources, however, I primarily play in a 1st/2nd ed. campaign, thats been ongoing since the late 70's.
- `spells.json` is the final form for each spell.
 - The information for each spell is a dictionary using double quotes `""`
- `mem_spell.txt` is a raw form of the text after it's processed by `pytesseract`
 - This is a staging area to clean the text, which can include the following
 - Fix incorrectly OCRed words
 - Format text with newlines `\n\n` to split paragraphs
 - Format tables with tabs `\t` and `\n` to align columns and now space between rows
 - Change `:` to `|` to split `key` and `value`.  The text description can contain `:`, so it's not feasible to split on `:`
 - One blank row between each spell in this file
 - Once cleaned and formatted, use code in the notebook to convert each spell into a `dict`, so I don't have manually copy and paste
 - Probably some stuff I'm forgetting
 
 ## Tools
 - Jupyter Lab
  - Currently, my notebook is a tad messy.
  - A section of code is used to OCR a pdf of my resource
  - A section to clean the spell description and read each spell in the file, `mem_spell.txt`, into a `dict` to add into `spells.json`
  - There's a lot of manual cleaning of text, but not as much as if you had to type in the entire spell
  - If you can improve the automated part, great!  However, I'm mostly interested in just getting each spell into a `dict`
  - `{"Name": "", "Class": [], "School": [], "Level": "", "Range": "", "Components": [], "Casting Time": "", "Duration": "", "Area of Effect": "", "Saving Throw": "", "Description": ""}`
 - Python 3.7 until the Anaconda distribution updates to 3.8
 - [`tesseract`][1]
  - [tesseract wiki][2]
  - [windows installation][3] from UB Mannheim
 - pytesseract

 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  [1]: https://github.com/tesseract-ocr/tesseract
  [2]: https://github.com/tesseract-ocr/tesseract/wiki
  [3]: https://github.com/UB-Mannheim/tesseract/wiki