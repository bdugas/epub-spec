# Kobo ePub Specifications
What’s in this Document:
 
* Elements of the ePub spec that Kobo does and does not support.
* Features of the five Kobo reading platforms.
* Recommendations on file production and testing for content creators. 
 
 
### Disclosure and Confidentiality
This document contains confidential and proprietary information of Kobo Inc. Its receipt or possession does not convey any ownership rights therein, or any rights to reproduce or disclose its contents or to manufacture, use, or sell it or anything it may describe. Reproduction, disclosure, or use without specific written authorization of Kobo Inc. is strictly forbidden. Kobo Inc. reserves the right to update this document without notice to its client vendors unless otherwise agreed to.

### Table of Contents

1. [ePub Versions Kobo Supports](#epub-versions-kobo-supports)
2. [Kobo Reading Platforms](#kobo-serves-content-to-users-on-these-5-reading-platforms)
3. [Kobo Devices](#current-kobo-devices)
5. [Kobo Recommends Initial ePub Check](#kobo-recommends-initial-epub-check)
6. [Sideloading for Testing Purposes](#sideloading-for-testing-purposes)
7. [Digital Rights Management (DRM)](#digital-rights-management-drm)
8. [Placing Images Properly](#placing-images-properly)
9. [Cover Images](#cover-images)
10. [Scalable Vector Graphics (SVG)](#scalable-vector-graphics-svg)
11. [Table of Contents (ToC)](#table-of-contents-toc)
12. [OPF](#opf)
13. [Supported Fonts](#supported-fonts)
14. [Obfuscated Fonts](#obfuscated-fonts-are-not-currently-supported-by-the-kobo-cms)
15. [Embedded Fonts](#embedded-fonts-can-be-selected-by-users)
16. [Languages](#languages-other-than-english)
17. [Footnotes/Endnotes](#footnotesendnotes-are-fully-supported-across-kobo-platforms)
18. [Fixed Layout](#fixed-layout-fxl-support)
19. [SMIL](#kobo-supports-smil)
20. [Image-Based FXL Reader](#image-based-fxl-reader)
21. [Multimedia Support / Media Overlays](#multimedia-support--media-overlays)
22. [JavaScript Support](#javascript-support)
23. [MathML](#mathml-is-supported-on-ios-elnk-and-desktop-platforms)
24. [Fallback Statements/Switches](#fallback-statementsswitches)
25. [ePub Previews](#epub-previews)
26. [Tables](#tables)
27. [Support Grid] (#support-grid)
28. [Questions?](#still-have-questions)

### ePub Versions Kobo Supports
 
Kobo supports ePub, the universal open standard eBook format maintained by the Independent Digital Publishing Forum [(IDPF)](http://idpf.org/epub). The current version is ePub 3 but Kobo still supports its predecessor, ePub 2.0.1.
 
The ePub 3.0 spec is based on HTML5 and CSS3, adhering to the most recent versions. Content creators are advised to review the [HTML5 and CSS3 reference profiles](http://www.idpf.org/epub/30/spec/epub30-contentdocs.html#references) because changes to them could impact file production. 
 
Kobo supports a subset of elements from the ePub 3.0 spec. The following covers which elements are supported across Kobo’s reading platforms.
 
### Kobo Serves Content to Users On These 5 Reading Platforms 
 
1. eInk/EPD — Kobo eInk devices (Aura, Glo, Touch) 
2. Desktop — the Kobo desktop app for PC and Apple Computers
3. Android — all Android devices running the Kobo app including all Kobo Arc versions
4. iOS — iPad, iPhone and iPod Touch
5. Windows 8 — all tablets, smartphones and computers running Windows 8.

### Current Kobo Devices
 
Android: 
* Arc 7 SD
* Arc 7 HD
* Arc 10 HD

eInk:
* Aura
* Aura HD
* Aura HD
* Glo

### Earlier Kobo Devices
 
Android:
* Arc (original)
* Vox

eInk:
* Kobo Mini
* Touch
* Kobo WiFi
* Kobo1
 
### Kobo Recommends Initial ePub Check 
 
The Kobo CMS does not use a built in ePubCheck. To detect errors in ePubs, the IDPF provides both a [web validation tool](http://validator.idpf.org/) and a [desktop application](https://github.com/IDPF/epubcheck). Kobo cannot guarantee that files that fail ePubCheck will render correctly across its reading platforms. So ePubs should be validated using the most recent version of ePubCheck prior to distribution. 
 
The Kobo Content Management System will neither reject those files that fail ePubCheck nor send reports to their publishers. However, if any rendering or performance issues harm the user experience, the files may be flagged for, and then failed in, the Kobo content QA process.

### Sideloading for Testing Purposes
 
Kobo encourages the testing of content on all its reading platforms. However, sideloading is currently supported on eInk, Android and iOS. Here’s how to sideload content:
 
**eInk**

1. Connect the device to your computer via USB.
2. Find the drive on your computer in Finder or Windows Explorer.
3. Drag your ePub onto the device. To trigger the Kobo WebKit, change the file extension to “.kepub.epub”. To trigger the Kobo Webkit for a Fixed Layout title, change the extension to “.fxl.kepub.epub”. (If the extension is left unchanged it will render using the Adobe Digital Editions Webkit.)
4. Disconnect your device. The file will automatically appear in your library.
 
**Desktop**

1. Open the Kobo Desktop app.
2. Make sure you have [Adobe Digital Editions](http://www.adobe.com/ca/products/digital-editions/download.html) installed. 
3. Select the Library tab and press CTRL+Shift+S on Windows or ⌘+SHIFT+S on a Mac. This will display any files in the “My Digital Editions” folder on your computer with the extension .kepub.epub or .fxl.kepub.epub
 
**Android**

1. Connect the device to your computer via USB.
2. Find the drive on your computer in Windows Explorer. If you use a Mac, install and connect to the device using [Android File Transfer](http://www.android.com/filetransfer/).
3. Drag your ePub onto the device.
4. On the device, navigate to the Kobo App or, if you use a Kobo Arc, the Books Collection. Select options (the three dots on the top right) then “Import”.
5. Once the files appear, confirm that you want to import them. They will display in your library.
 
**iOS**

1. Connect the device to your computer with the iOS cable.
2. Open iTunes and navigate to iPad -> Apps.
3. Select the Kobo app from the box on the left.
4. Drag the ePub to the box in the bottom right of your iTunes window. The file will then automatically import and display in your library.

(The Kobo iOS app is registered among apps that open epub and pdf files. Users can use the standard “open in…” menu from Safari, Dropbox, or any other app that supports it to view their files.)
 
**Windows 8**

1. Open the Kobo app, navigate to the Library and swipe up from the bottom of the screen.
2. Select “import”.
3. Select the files on the device that you want to import. (The Kobo app will scan all the files on your device that it can import. You may not be able to transfer files via USB depending on the specific Windows 8 device and may need to transfer them by OneDrive, Dropbox, email or some other method instead.)
4. Select “Open” and wait for the files to load into your library.

### Digital Rights Management (DRM)
 
ePubs loaded to the Kobo store are protected by Kobo DRM. Kobo can turn the DRM off at the publisher-level, when publishers make a request to the Publisher Operations team.
 
Kobo’s DRM system hosts content on its reading platforms using advanced security methods, including the use of encryption and hash algorithms. Various keys are used to encrypt content before it is sent to the reading platform. There are unique keys for each eBook, user and device. 
 
At a minimum, Kobo employs encryption standards in the 128-bit version of the Advanced Encryption Standard (AES) of the US Government.
 
### Placing Images Properly
 
Kobo reading platforms support the core image types outlined in the [IDPF spec](http://www.idpf.org/epub/30/spec/epub30-publications.html#cmt-grp-image). This includes JPG, PNG and GIF but not Scalable Vector Graphics (SVG), which are not supported on all reading platforms. (See the Support Grid.) PNG files are preferred over JPG.
 
All images should use the RGB color model, and not CMYK. Encapsulated PostScript (EPS) images are not supported on Kobo.
 
**The advised maximum size for all image types is 3 MB.** ePubs with larger images are still accepted and those images will not cause Kobo apps and devices to crash. However, ePubs with images all under this limit perform optimally across platforms.
 
**Image widths in the Cascading Style Sheets (CSS) should be set in pixels instead of percentages.** Images with widths set by percentages may stretch in landscape orientation on tablets or other devices. Kobo reading platforms insert max-width and max-height CSS for images and video. This ensures they’re not split over multiple pages.
 
For a full screen image view on the Android and iOS platforms, users can long press images in reflowable ePubs. Once in full-screen view, users will be able to pinch and zoom.

### Cover Images
 
If an external cover image is uploaded to both the Kobo system and the ePub, that external image displays as the thumbnail image in the store and in user’s libraries. The internal ePub cover still displays when the user opens the file on their device.
 
GIF files are not supported for covers.
 
The suggested optimal ratio for covers on Kobo is 3:4 width:height. (The average size and dimensions for ebook covers in the Kobo store are 800:1224px width:height.) However covers in all dimensions will be rendered consistently across platforms. Content creators are advised to keep their cover images under 3MB. Larger covers will still render but will not improve the display of their content.
 
### Scalable Vector Graphics (SVG)
 
SVG is partially supported across Kobo platforms. Thorough testing is advised for ePubs with SVG, particularly for text rendering. Content creators are advised to use the [ePub switch element](http://www.idpf.org/epub/30/spec/epub30-contentdocs.html#elemdef-switch) to provide fallback content. Refer to the support grid in this document or the test results for Kobo's reading platforms at [ePubtest.org] (http://www.epubtest.org).
 
### Table of Contents (ToC)
 
**For ePub 2.0.1**, Kobo reading platforms populate the ToC menu in the book with the ToC from the file toc.ncx (which is in navMap). However, if the toc.ncx is not present, the TOC menu is populated by the Spine listing in the OPF.
 
When an OPF-spine item is not listed in the TOC.ncx, the Kobo CMS will create a listing for it using the filename or the opening words from the section. This listing will be displayed to the user in the TOC Menu across all reading platforms. This process may be removed in a future release. ePubs that use a nav.html TOC will not be impacted. 
 
**For ePub 3.0**, Kobo platforms will read the ToC from the ToC table in the nav.html file. When a ToC table is not present, the next available table will be used. If the nav.html is not present, it will populate the ToC with the toc.ncx. If the toc.ncx is not present, it will populate the ToC with the spine listing in the OPF.
 
The hidden attribute can be used to prevent the ToC listing from appearing in the ePub body while still displaying in the ToC menu. ToC menus on Kobo platforms support nesting up to three elements deep.

### OPF
 
The Kobo CMS reads the external metadata provided by the publisher. So most fields in the metadata section of the OPF file are not read. The one exception is the <dc:identifier>. It should contain the eBook ISBN, also supplied in the external metadata. However, if this field does not contain the eBook ISBN, it must be in the ePub file name.
 
Kobo uses external metadata files to populate the various metadata fields on the Kobo website. The ISBN in the <dc: identifier> field in the OPF file matches the ePub to the external metadata entry. If there is no ISBN in the <dc: identifier> tab, Kobo looks for the ISBN in the ePub filename. The ISBN from the external metadata must match either the <dc: identifier> field or the ePub file name.
 
**Content creators are advised to use [tags for manifest items](http://www.idpf.org/epub/30/spec/epub30-publications.html#sec-item-property-values)**, specifically the cover tag. Some of these are read across Kobo’s reading platforms and future developments will be able to take advantage of properly tagged items.
 
**Special characters and spaces should not be used** for file names within an ePub. This will result in the naming inconsistencies with the items listed in the OPF manifest. Special characters are not letters or numbers (ex: # or ?).

### Supported Fonts
 
TTF and OTF font types are fully supported on Kobo. Other font types are not supported as per the ePub spec.
 
**Font customization options available to Kobo users** on each reading platform:
 
**Android:** Droid Sans Serif, Droid Serif
 
**Desktop:** A-OTF Gothic MB101 Pr6N R, A-OTF Ryumin PR6N R-KL, Arial, Ariel Narrow, Arial Unicode MS, Calibri, Calibri Light, Cambria, Cambria Math, Constantia, DFKai-SB, Georgia, KaiTi, Lucida Sans, Palatino Linotype, Meiryo, Meiryo UI, MS Gothic, MS Mincho, MS PGothic, MS PMincho, SimHei, Times New Roman, Tahoma, Trebuchet MS
 
**eInk:** Amasis, Avenir Next, Caecilia, Georgia, Gill Sans, Kobo Nickel, Malabar, Gothic, Ryumin, Dyslexie, OpenDyslexic ([optimized for dyslexic readers](http://opendyslexic.org/))
 
**iOS:** Avenir, Baskerville, Cochin, Georgia, Helvetica, Optima, Palatino, Trebuchet, Verdana
 
**Windows 8:** Cambria, Calibri, Georgia, SegoeUI, Times New Roman, Trebuchet MS, Verdana.

### Obfuscated Fonts Are Not Currently Supported by the Kobo CMS
Non-sideloaded titles with obfuscated fonts will display the reading platform’s default font instead of the intended font. As a result they may fail content QA. However, work is underway at Kobo to support obfuscated fonts and render these titles correctly.

### Embedded Fonts Can Be Selected By Users 
When opening a new book, the font that displays is the one chosen by the user for their previous open book. For an embedded font, users can select “Document Default” or “Publisher Default” from the font options. The exception is FXL content for which users cannot choose their font. Fonts in FXL content are determined by the CSS in the ePub.

If the reading experience of a book requires that the embedded font be used, consider adding a note to the front matter. Instruct the user to select the “Document Default” font option. 

**To avoid text-positioning errors**, seriously consider embedding and specifying fonts in the CSS for all fixed layout ePubs. If fonts are not embedded and specified, the reading platform defaults to Times. Fixed layout files that use the default font should be tested extensively on Kobo’s reading platforms.

### Languages Other Than English
 
When a user selects an available default font, Kobo reading platforms may not correctly render all glyphs within the script. So Content containing glyphs not present in Kobo’s default apps should be tested across platforms. Creators may want to embed a font that contains the glyphs used in their content to ensure it renders correctly.
 
Some glyphs do not render on most fonts. In cases where creators are unable to supply embedded fonts they can insert a note into the front matter of their content instructing users to select the font Georgia. It correctly renders the greatest set of scripts.
 
Kobo is currently working to add built-in fonts to the eInk and Android-reading platforms and render glyphs from all scripts correctly. The Desktop, iOS and Windows 8 platforms already contain built-in fonts that will render glyphs from all scripts.

### Footnotes/Endnotes Are Fully Supported Across Kobo Platforms
 
Users of the eInk and iOS platforms see a pop-up text box containing a footnote or endnote’s text. They can also navigate to the HTML section with the content. All other platforms simply link the user to the HTML section with the reference text.
 
It is strongly recommended that reference notes use the appropriate [ePub:type identifying attribute](http://www.idpf.org/epub/30/spec/epub30-contentdocs.html#sec-xhtml-content-type-attribute). This way Kobo platforms can interpret them correctly.
 
The iOS footnote pop-up renders more than just plain text, including images and tappable links. Simply place all the contents of the footnote within the element being linked to.

### Fixed Layout (FXL) Support
 
Kobo supports the [official ePub3 FXL spec](http://www.idpf.org/epub/fxl/). This includes such features as [Right-to-Left Reading](http://www.idpf.org/epub/30/spec/epub30-publications.html#attrdef-spine-page-progression-direction), SMIL/Read Along, and various rendition-spread options. The [rendition:layout property](http://www.idpf.org/epub/fxl/#property-layout) in the OPF determines the layout of the content and is read by all of Kobo’s platforms.
 
Kobo platforms also read the field <option name=”fixed-layout”>true/false</option> to identify whether ePubs should be rendered as FXL. The file containing this field is usually titled com.kobobooks.display-options.xml and can be found in the META-INF directory of the ePub.
 
All five values in the [rendition:spread property](http://www.idpf.org/epub/fxl/#property-spread) are also supported. However rendition-spread properties are only read at the book level. Future versions of Kobo’s reading platforms may read the rendition:spread and rendition:layout properties at the spine level.
 
**Pinch and zoom gestures** are present on the Android, iOS, and Windows 8 reading platforms. Zooming is possible on eInk devices by accessing the reading menu and zooming. Zooming is not supported on the Kobo Desktop app.
 
FXL content on Android always displays one page in portrait view.

**Kobo strongly advises against the use of inline styling for FXL content**. Text boxes with inline styling may render inconsistently across platforms, resulting in text overlapping or incorrect positioning.
 
**Kobo also advises against using images where the width or height (in pixels) exceed the dimensions of the viewport**. ePubs containing images that exceed the viewport dimensions may not render correctly on the eInk platform.

### Kobo Supports SMIL
 
[SMIL (Synchronized Multimedia Integration Language)](http://www.idpf.org/epub/30/spec/epub30-mediaoverlays.html#sec-smil-smil-elem) is supported for FXL titles on Android and iOS. Audio files must be encoded using Apple iTunes AAC-LC mp4-v2 codec, 256 kbps.
 
Note: the Kobo Android platform **does not currently support**:

* Non-Linear playback
* Text highlighting for SVG text
 
When the rendition:spread property is set to “none” or “auto”, Android displays a full spread in FXL Read Along content in landscape.
 
Custom text colors for highlighting are not currently supported on Android. However, custom text colors for highlighting is possible on iOS. The iOS app uses the CSS class ‘kobo-smil-highlight’ to color highlighted text. So, by adding that class to the CSS plus a color declaration, the color of the highlighted text on the app can be customized.

### Image-Based FXL reader
 
The Kobo Android and iOS platforms will render FXL ePubs that meet certain criteria with an image-based fixed layout reader. This reader features significantly faster panning, zooming, and page-turns than the standard one. Designed to enhance the reading experience of comics, it works for any FXL ePubs composed entirely of images.
 
**ePubs that meet the following criteria will be displayed with the image-based reader on Kobo’s iOS and Android platforms**:

1. The content is fixed-layout.
2. The ePub does not contain SMIL content.
3. An image must be available for each spine item. Spine items are inspected for images using these rules — and each spine item must contain one of the following formats:
<ul>
<li>a. either a non-SVG image (e.g. PNG)</li>
<li>b. or an SVG image with a non-SVG image fallback provided in the manifest. In this case, the fallback image is used in the comics renderer</li>
<li>c. or an HTML file which falls under one of the following categories:
<ul>
<li>i. either it contains a single ‘img’ tag which references an image. In this case, this image will be used</li>
<li>ii. or it contains a svg definition with an ‘image’ child tag referencing an image. In this case, the referenced image will be used. NB: embedded object tags (‘object’), which may include an SVG image in the ‘data’ attribute, do not fall into this category</li>
<li>iii. or an HTML page which contains no child elements under ‘body’. This item will be rendered as a blank white page.</li></ul></li></ul>
4. The same image cannot appear twice in a row. If two consecutive pages refer to the same image, the platform will assume that CSS styling is repositioning the image, which is not supported by the image-based FXL reader.
 
For example, a file that lists spine items, manifest items, and contains nothing but an image in the HTML body will trigger the image-based renderer.
 
First spine item:<br>
`<spine page-progression-direction="ltr" toc="ncx">`<br>
`<itemref idref="page0-xhtml" linear="yes"/>`

Matching item in manifest:<br>
`<item id="page0-xhtml" href="contents/Page00.xhtml" media-type="application/xhtml+xml"/>`
 
HTML body for item:<br>
`<body>`<br>
`<div id="layer0">`<br>
`<image width="1076" height="1394" xlink:href="../images/Image01-1-0.jpg"/>`<br>
`</div>`<br>
`</body>`
 
If images are set using the [background property](http://www.w3.org/TR/CSS21/colors.html#propdef-background) of elements the platform will fall back to using the default reader.
 
On Android, if the image is determined to be twice as large as the screen in any dimension, a low-res version of the image loads when the user turns a page. Within a second, the high-res version replaces the original image. This optimization prevents memory issues when users quickly flip through pages. The low-res image might appear slightly blurry or soft compared to the final hi-res image.

### Multimedia Support / Media Overlays 
 
Testing across platforms for ePubs with multimedia and other media overlays is recommended.
 
Embedded audio and video is currently supported on Kobo’s iOS platform for all content, but on the Android platform for FXL content only. The next version of the Android app (5.5) will support embedded audio and video as well as JavaScript for reflowable content as well.
 
Windows 8 does not currently support embedded audio and video. Kobo eInk devices and the desktop app do not support embedded audio and video either but will display any content included as a fallback using the [switch element](http://www.idpf.org/epub/30/spec/epub30-contentdocs.html#elemdef-switch) display instead.
 
### JavaScript Support
 
Kobo’s Android platform supports JavaScript for fixed-layout ePubs. Kobo’s iOS platform supports JavaScript for both reflowable and FXL ePubs. ePubs with JavaScript should contain fallback statements. This way, platforms that do not support JavaScript can still produce a coherent reading experience. Thorough testing on all platforms is strongly recommended to ensure that fallback as well as JavaScript content renders correctly.
 
### MathML is Supported on iOS, elnk, and Desktop platforms
 
Please note that [MathML](http://www.idpf.org/epub/30/spec/epub30-contentdocs.html#sec-xhtml-mathml) is not presently supported on the Kobo Android or Windows 8 platforms. Kobo recommends using [fallback statements](http://www.idpf.org/epub/30/spec/epub30-contentdocs.html#elemdef-switch) in ePubs with MathML components to ensure a comprehensible reading experience across platforms.

### Fallback Statements/Switches 
 
All Kobo platforms read fallback statements as outlined in the [IDPF spec](http://www.idpf.org/epub/30/spec/epub30-publications.html#sec-fallback-processing-flow). However, some devices and apps do not yet or cannot support audio/video, JavaScript, MathML or other “enhanced” elements. It is strongly recommended that ePubs with these elements use fallback statements to ensure that they are accessible to readers.
 
For example:
 
<pre><code>&lt;!--&lt;epub:switch id=&quot;c01-mdis-0001&quot;&gt;
 &lt;epub:case required-namespace=&quot;http://www.w3.org/1998/Math/MathML&quot;&gt;
   &lt;span class=&quot;equation&quot;&gt;
     &lt;span class=&quot;equation-line&quot;&gt;
       &lt;span class=&quot;equation-label&quot; style=&quot;margin-top:0.02384993em&quot;&gt;(1.1)&lt;/span&gt;
       &lt;span class=&quot;equation-content&quot;&gt;
         &lt;math display='block' xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;&gt;
&lt;mrow&gt;&lt;msub&gt;&lt;mi&gt;V&lt;/mi&gt;&lt;mn&gt;1&lt;/mn&gt;&lt;/msub&gt;&lt;mo&gt;+&lt;/mo&gt;&lt;msub&gt;&lt;mi&gt;Z&lt;/mi&gt;&lt;mi&gt;s&lt;/mi&gt;&lt;/msub&gt;&lt;msub&gt;&lt;mi&gt;I&lt;/mi&gt;&lt;mn&gt;1&lt;/mn&gt;&lt;/msub&gt;&lt;mo&gt;=&lt;/mo&gt;&lt;msub&gt;&lt;mi&gt;V&lt;/mi&gt;&lt;mi&gt;s&lt;/mi&gt;&lt;/msub&gt;&lt;/mrow&gt;&lt;/math&gt;&lt;/span&gt;&lt;/span&gt;&lt;/span&gt;
    &lt;/epub:case&gt;
     &lt;epub:default&gt;--&gt;
   &lt;p class=&quot;para_center&quot;&gt;
     &lt;img id=&quot;c01-mdis-0001&quot; src=&quot;images/m001.gif&quot; alt=&quot;&quot;/&gt;
   &lt;/p&gt;
   &lt;!--&lt;/epub:default&gt;
&lt;/epub:switch&gt;--&gt;
</code></pre>
 
In the above, the parts of the switch which legacy viewers would not be able to handle have been called out. So platforms that do not support MathML display the fallback content instead. 

### ePub Previews 
 
Publishers can set the amount of content they make available in previews. They use their metadata feed or work with Kobo’s Publisher Operations team to customize their account settings.
 
**On the account level**, previews are set to display 5% of the ePub’s content by default. Previews can be turned on or off. The maximum percentage that accounts can be set to is 25%.
 
**On the product level**, the default is 5%. Publishers can set preview percentages for individual titles. They can use the Kobo Excel metadata template or ONIX 3.0 with the tags EpubUsageType, EpubUsageStatus or EpubUsageLimit. Previews can be set between 0% and 25%.
 
Publishers can also upload custom previews by using the naming convention ISBN_preview.epub in the preview files they distribute.
 
### Tables 
 
Sometimes tables wider than four columns may not be readable in reflowable ePub files, particularly on eInk devices. Content producers adding tables with more than four columns are advised to test their content on all Kobo reading platforms. Likewise, when HTML tables do not render as intended, they can reformat or capture the tables as high-resolution images.
 
### Limitations and Maximums 
 
Kobo recommends the following limits for ePub file and component size. Files exceeding these sizes will not necessarily fail to load to the Kobo store. Moreover, large files that successfully load to the store will not degrade app performance. Larger files will simply take longer to download to users’ devices and use more memory.
 
* 3 MB/image in FXL and Reflowable ePubs
* 1 GB/ePub
 
### Support Grid

The following table lists features supported by at least one Kobo platform but not uniformly supported across all platforms. Features not listed here are either supported across all platforms or not supported on any platforms.

| Platform | MathML | SMIL | JavaScript | CSS Animations | Audio/Video |
|----------|--------|------|------------|----------------|-------------|
| Android  | N      | Y    | Y          | Y              | Y           |
| Desktop  | Y      | N    | Y          | Y              | N           |
| eInk     | Y      | N    | Y          | Y              | N           |
| iOS      | Y      | Y    | Y          | Y              | Y           |
| Windows8 | N      | N    | N          | N              | N           |

### Still have questions? 
 
Learn more about Kobo’s ePub support at [epubtest.org](http://epubtest.org/). It’s categorized into required and optional features. 
 
Or email questions to pubops@kobo.com, including “ePub Spec” and the section title related to your query in the subject line.
