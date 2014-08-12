Translations
============

Translation files used across the SkedGo family of products

You are very welcome to contribute:

1. Fork this repository (button in top right of this page)
2. Edit the file in your fork
3. Submit a pull request


# Translating .strings files

## Opening the file

Open the file in a plain text editor. Not Word or Pages but one which can modify plain text files like Notepad or TextEdit.


## Translating the file

The files are a list of items which need to be translated where each item has the following structure:

    /* Comment meant to help to translate */
    "Internal Key" = "Translation";

For example:

    /* Action title for adding a vehicle */
    "Add vehicle" = "Add vehicle";

You have been provided with the files used for the English translation of the app. In many cases the 'Internal Key' is the same as the 'Translation' in that case. Your task is to translate the 'Translation' bit. Modify the file directly and adjust what's in the double quotes directly. Keep the double quotes and the semicolon.

So the above translated to German would be:

    /* Action title for adding a vehicle */
    "Add vehicle" = "Fahrzeug hinzufügen";

If it's unclear what the context of the 'Internal Key' and the comment doesn't help, please let us know.


## Translating formats and percentage signs

Some translations are for text snippets where the code will insert additional text or numbers when the app is running. These are called format strings and will have placeholders in the 'Translation' part.

For example:

    /* Action title for calling taxi provider of %name */
    "CallTaxiFormat" = "Call %@";

The '%@' is the placeholder. The app will injoect the name of the taxi provider in this case. You can move around the placeholder.

In German this could be:

    /* Action title for calling taxi provider of %name */
    "CallTaxiFormat" = "%@ anrufen";

If there are multiple placeholder, and you need them in a different order, you can change the order by inserting numbering. The numbering starts at 1. So the following:

    /* From %date1 to %date2 */
    "DateFromToFormat" = "From %@ to %@";

Could be translated as:

    /* From %date1 to %date2 */
    "DateFromToFormat" = "Bis %2$@; ab %1$@“;

(Note that the semicolon after %2$@ is part of the translation, i.e., it will be visible in the app.)


# Translating .properties files

The .properties files follow a similar mechanism but have the structure

    # Comment meant to help to translate (optional)
    Internal Key=Translation"

Where placeholders are using curly braces and numbering begins at 0 (!):

    stay.on.<vehicle>.at.<from>.to.<to>=Stay on {0} at {1} to {2}

**Note**: .properties files must be in ISO-8859-1. You can create the files in UTF-8 and use `native2ascii` to convert them or just append to '.utf8' to the filename, to indicate to us that it needs conversion.


# Tips and trips

- If you're using your phone in a different language than the one you're translating to, it's good practice to switch it to the language that you want translate to. That gives you a better feel of the appropriate terminology.
- Also a good help is using VoiceOver on your device, which allows reading out screen content. On iOS go to the Settings App => General => Accessibility => Accessibility Shortcut (at the bottom) => Voice Over, then you can enable/disable VoiceOver by triple-tapping the home button.
