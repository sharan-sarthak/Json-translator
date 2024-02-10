**Introduction**
This Python Script allows you to translate the JSON documents from source to destination language. 

The user can select the source or destination language.

**Downloads and Imports**
An IDE is needed, PyCharm is recommended. Download the Community version Download PyCharm: Python IDE for Professional Developers by JetBrains 

Python version 3.8 or 3.9 is used

Imported certain libraries: 

Json library - for reading or writing into .JSON files

GoogleTrans library - for translation

to install the GoogleTrans library the run this command in terminal - pip install googletrans==3.1.0a0 

Re library - for checking the regex

**Limitations**
This translation python script ignores the JSON values which contains HTML tags and Dynamic Variables means this script ignores all the values which contains regex.

And translation for these values should be done manually.

**File Structure** 
Inside the Python package there 1 file present that is

main.py - Execution starts from here, that reads a JSON file and then the translation is done.

**Working**
The execution starts from the main.py file

At first, fileReader() is called and after reading the JSON it is stored in the x variable

Now this x variable which contains the JSON is passed for the translation like this translateValues.translateDict(x)

After the translation is done the JSON is wrote back to the new file this is the translated one by the function call fileWriter(x)

 

For reading the JSON and writing the JSON into the file - there are two functions implemented: 

fileReader() - Reads the JSON and stores it into x variable by opening the file in "rb" method

fileWriter(x) - Writes the x which contains the JSON into the file by opening it into "wb" method

 

For Translation of the values three functions are implemented here:

translateDict(x) - This iterates the dictionary, and the value v is then checked that it is a String or a Dictionary. For this a function is called isDictOrString(v). If the value v is dictionary, then call the same function again x[k] = translateDict(v) and if the values v is string, then call x[k] = translateString(v)

isDictOrString(x) - type of the value x is checked if it is String return False else return True

translateString(v) - this is the function where the translation is done. 

First of all, before the translation is done the regex is checked

If the value v doesn’t contain the regex, then the translation is done, and the translated value is returned.

**Execution Steps**
Here are the steps to execute the Translation’s executable file:

Download the main.exe executable file from the files attached below

Now, double click the main.exe and execute it

The console will open and it will ask for the Source Language and Destination Language as an input from the user

Provide the source language and destination language codes as per the Supported Languages list

After this the path has to be entered by the user which has the JSON files that are to be translated

Now, on the console there would be the values printed which are getting translated

After the execution is completed, there would be 1 folder(output_JSON) and 1 file(log file) generated in the same directory as of main.exe

The generated folder named output_JSON contains all the translated files

The another generated file would be translationModule.log file – this log file includes all the values which contains the HTML tags and Dynamic Variables and which are nnot translated

The non-translated values for all the files are separated by the names of the files in the same log file

All these HTML tags and Dynamic Variables contained values should be translated manually

**Supported Languages**
Here is the list for the supported languages for googletrans library,

'afrikaans': 'af',
'arabic': 'ar',
'belarusian': 'be',
'bulgarian': 'bg',
'catalan': 'ca',
'czech': 'cs',
'welsh': 'cy',
'danish': 'da',
'german': 'de',
'greek': 'el',
'english': 'en',
'esperanto': 'eo',
'spanish': 'es',
'estonian': 'et',
'persian': 'fa',
'finnish': 'fi',
'french': 'fr',
'irish': 'ga',
'galician': 'gl',
'hindi': 'hi',
'croatian': 'hr',
'hungarian': 'hu',
'indonesian': 'id',
'icelandic': 'is',
'italian': 'it',
'hebrew': 'iw',
'japanese': 'ja',
'korean': 'ko',
'latin': 'la',
'lithuanian': 'lt',
'latvian': 'lv',
'macedonian': 'mk',
'malay': 'ms',
'maltese': 'mt',
'chinese_simplified': 'zh-CN',
'chinese_traditional': 'zh-TW',
'auto': 'auto'

Here is the **Github reference page** : GitHub - Scoefield/GoogleTransLibrary: Learning how to make pyhton third-party library for PIP installation with Google translation spider - https://github.com/Scoefield/GoogleTransLibrary#support-language

**Known Issues**
Here is the StackOverFlow page for the issues occured (if any) while installing or working of the GoogleTrans library.

googletrans stopped working with error 'NoneType' object has no attribute 'group' - https://stackoverflow.com/questions/52455774/googletrans-stopped-working-with-error-nonetype-object-has-no-attribute-group
