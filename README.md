# AndroidApp

This is a  better template for .NET Android projects.

## Why?

The **.NET Android application** template provided in **Visual Studio** had some minor issues, so I tried to do this.

### What was changed?

Most of the files have been modified to be as neat as possible and consistent with Google's Android project.  Don't worry, I've kept the best of both.

The following references are used:

https://learn.microsoft.com/xamarin/android/deploy-test/building-apps/build-properties

https://developer.android.com/guide/topics/manifest/manifest-intro#example

https://developer.android.com/guide/topics/resources/layout-resource

https://developer.android.com/guide/topics/resources/string-resource

https://developer.android.com/develop/ui/views/launch/icon_design_adaptive

https://github.com/android/uamp

https://github.com/android10/Android-CleanArchitecture

## More Info

### Icon

[icon.png](images/icon.png) is the icon of the template.

The app icon is from https://icon.kitchen/i/H4sIAAAAAAAAAx3MOw6AIBBF0b282hW4De2MxeiMQOSjICaGsHfF8p7iFtxksyT0BUxxH7U4Qb%2BRTdJhUeNzfAkViY34C80GTT%2BmM5u4WkHt4AJn2zYTyHMMhjHXF%2BIOlK9dAAAA

### AboutResources.txt

```
Images, layout descriptions, binary blobs and string dictionaries can be included 
in your application as resource files.  Various Android APIs are designed to 
operate on the resource IDs instead of dealing with images, strings or binary blobs 
directly.

For example, a sample Android app that contains a user interface layout (main.xml),
an internationalization string table (strings.xml) and some icons (drawable-XXX/icon.png) 
would keep its resources in the "Resources" directory of the application:

Resources/
    drawable/
        icon.png

    layout/
        main.xml

    values/
        strings.xml

In order to get the build system to recognize Android resources, set the build action to
"AndroidResource".  The native Android APIs do not operate directly with filenames, but 
instead operate on resource IDs.  When you compile an Android application that uses resources, 
the build system will package the resources for distribution and generate a class called "Resource" 
(this is an Android convention) that contains the tokens for each one of the resources 
included. For example, for the above Resources layout, this is what the Resource class would expose:

public class Resource {
    public class Drawable {
        public const int icon = 0x123;
    }

    public class Layout {
        public const int main = 0x456;
    }

    public class Strings {
        public const int first_string = 0xabc;
        public const int second_string = 0xbcd;
    }
}

You would then use Resource.Drawable.icon to reference the drawable/icon.png file, or 
Resource.Layout.main to reference the layout/main.xml file, or Resource.Strings.first_string 
to reference the first string in the dictionary file values/strings.xml.
```

