# Shortcodes List

## 1. Carousel01

Image carousel for **global resources**.

### Usage

    {{< carousel01 size="450x" >}}
    path/to/image1.jpg:link_title:target_link
    path/to/image2.jpg:link_title:target_link
    path/to/image3.jpg:link_title:target_link
    {{< /carousel01 >}}

## 2. carousel02

Image carousel for **local resources**.

### Usage

    {{< carousel02 size="450x" >}}
    path/to/image1.jpg:link_title:target_link
    path/to/image2.jpg:link_title:target_link
    path/to/image3.jpg:link_title:target_link
    {{< /carousel01 >}}

## 3. cushtml

To insert HTML in markdown file.

### Usage

    {{< cushtml >}}
    <div>your html here.</div>
    {{< /cushtml >}}

## 4. faqpair, faqques, faqans

To use them in *faq/{pagename}.md* file.

### Usage Example

    {{< faqpair >}}
    {{< faqques id="lih01-005" >}}
    Member List စာအုပ်မှာ ဘယ်လိုအချက်တွေပါပါသလဲ?
    {{< /faqques >}}
    {{< faqans >}}
    MGMA Member List စာအုပ်တွင် အသင်းဝင်စက်ရုံများ၏ အမည်၊ လိပ်စာ၊ ဆက်သွယ်ရန်ဖုန်းနံပါတ်၊ တင်ပို့သောနိုင်ငံ၊ ချုပ်လုပ်သောအထည်အမျိုးအစား၊ လုပ်သားဦးရေ စသည်တို့ ပြည့်စုံစွာ ဖော်ပြထားပါသည်။
    {{< /faqans >}}
    {{< /faqpair >}}

## 5. faqgroup

To use it in *faq/_index.md* file.

### Usage Example

    {{< faqgroup gid="qag01" hid="lih01" md="membership" >}}
    Membership
    {{< /faqgroup >}}

## 6. gstyle01

Gallery for **global resources** and **matching all**.

### Usage Example

    {{< gstyle01 src="path/to/*" tsize="250x" vsize="450x" >}}

## 7. gstyle02

Gallery for **local resources** and **matching all**.

### Usage Example

    {{< gstyle02 >}}

## 8. gstyle03

Gallery for **global resources** and **selected images**.

### Usage Example

    {{< gstyle03 tsize="250x" vsize="450x" >}}
    images/imgname01.jpg
    images/imgname02.jpg
    images/imgname03.jpg
    images/imgname04.jpg
    {{< /gstyle03 >}}

## 9. gstyle04

Gallery for **local resources** and **selected images**.

### Usage Example

    {{< gstyle04 tsize="250x" vsize="450x" >}}
    imgname01.jpg
    imgname02.jpg
    imgname03.jpg
    imgname04.jpg
    {{< /gstyle04 >}}

## 10. home-carousel01, home-carousel02

Above are obsolete.

## 11. lib

To put last pieces of a line in **display: inline-block;**.

### Usage Example

    ဖြစ်{{< lib "ကြပါသည်။" >}}

## 12. include-md

Use it in .md file to include content from a nother .md file.

### Usage Example

    {{< include-md "membership" >}}

## 13. include-partial

Use it in .md file to include partial template .html file.

### Usage Example

    {{< include-partial "homebody.html" >}}

## 14. istyle01

Insert image from **global resources**.

### Usage Example

    {{< istyle01 scr="path/to/image.jpg" size="350x" link="target_link" alt="sometext" class="image-style-one" >}}

## 15. istyle02

Insert image from **local resources**.

### Usage Example

    {{< istyle01 scr="path/to/image.jpg" size="350x" link="target_link" alt="sometext" class="image-style-one" >}}

## 16. supref

To put pieces of text and reference No. in **display: inline-block;** and **<sup></sup>** tag.

### Usage Example

    {{< supref word="some text" link="reference link No." target="target_link" >}}

## video-carousel01

Video carousel for **global resources** and **selected videos**.

### Usage Example

    {{< video-carousel01 >}}
    path/to/vidoe1.mp4:link_title:target_link
    path/to/vidoe2.mp4:link_title:target_link
    path/to/vidoe3.mp4:link_title:target_link
    {{< /video-carousel01 >}}

## video-carousel02

Video carousel for **local resources** and **selected videos**.

### Usage Example

    {{< video-carousel01 >}}
    path/to/vidoe1.mp4:link_title:target_link
    path/to/vidoe2.mp4:link_title:target_link
    path/to/vidoe3.mp4:link_title:target_link
    {{< /video-carousel01 >}}

