# Andover Email Templates for Campaign Monitor
The purpose of this github repository is to share the Phillips Academy Email Templates and Design/Usage guidelines. For use by Phillips Academy and contracted third-party designer/developer for creating official emails in Campaign Monitor.

https://www.campaignmonitor.com

## Email Template System
A custom email template system has been created to manage all templates. This development process is currently fluid.

### Applications Used
* Adobe Brackets
* Codekit 2.0
* Based on Campaign Monitor template code


## Copyright
These files are copyrighted by Phillips Academy and maintained by the Communications Office at Phillips Academy. The applications used are independent of Phillips Academy and do not endorse or support our work.


## Andover Email Styleguide

### Approval Process
All new email campaigns and template development must be approved by Andover Communications.

### Accountability
The third-party designer/developer will be accountable to deliver all email campaigns and templates on time and abiding by these requirements. Andover will not debug and fix errors, unless absolutely necessary.

### Philosophy

#### Coding Style
Andover email templates is code heavy. The reason for code heavy templates is to dictate to the email client as much style and layout structure as possible, so avoiding unexpected problems, i.e. Outlook issues. We highly suggest using this coding style in your development.

### Support Requirements

#### Responsive Development
All new email campaign and template development must be designed to work responsively across supported mobile, tablet, and desktop devices.

#### Litmus
All new email campaigns and templates must be tested on Litmus. The supported email clients are based on Litmus testing.

https://litmus.com


#### Supported OS

##### OS support based on Litmus testing:
* Android 2.3+
* iOS 7+
* Mac/PC

#### Supported Email Clients

##### Supported email clients (Class A):
* Apple Mail 7+
* Outlook 2000-2016
* Thunderbird 31
* Android 2.3, 4.2
* iPad and iPad Mini
* iPhone 5s+
* AOL (Explorer, Firefox, Chrome)
* Gmail (Explorer, Firefox, Chrome)
* Outlook.com (Explorer, Firefox, Chrome)
* Yahoo! Mail (Explorer, Firefox, Chrome)

##### Supported email clients (Class B):
* Android Gmail App
* Windows Phone

##### We do not support:
* Lotus (All Versions)
* Blackberry

##### Outlook Support:
Andover supports Outlook. Currently, our organization uses Outlook 2007-2010 as our main email client. Our organization will most likely review new email campaigns and templates in Outlook. Therefore, we work to make email campaigns and templates appear acceptable. Acceptable means we still provide a professional and Andover centric design in Outlook, but emails might look different because of Outlook’s limitations.


### Email/Template Requirements

#### Editable Campaign Monitor Templates
Campaign Monitor templates need to have editable regions. Instead of uploading a template per email campaign, all templates must be loaded into the Campaign Monitor template library for testing and use. This allows any of our trained Campaign Monitor users to use an approved template and build out an email campaign.

#### Images
Images must be responsive and work on supported devices and email clients. All images in template development, whether images or background images, must be uploaded with a template design.

#### Standard Font Styles
Serif font stack:

    font-family: Georgia, Times, serif;

Sans-serif font stack:

    font-family: "Helvetica Neue", Arial, Helvetica, sans-serif;

#### Custom Fonts
We like custom fonts. Feel free to use custom fonts in email as the design purposes. Custom font usage will need to be approved by Andover Communications.

#### Andover Seal & Wordmark
The Andover seal and wordmark must be used as provided. The Andover seal must not be used alone, EVER. The Andover wordmark can be used on its own in the absence of the seal and wordmark or if the seal and wordmark is used elsewhere in the email.

* Andover Seal & Wordmark: <a href="/html/images/andover-sealwordmark-2x-pablue.png">PNG</a>
* Andover Wordmark: <a href="/html/images/andover-wordmark-2x-pablue.png">PNG</a>

#### Andover Header
The standard Andover header should appear on all templates. The branding element font must not be changed. Any template without the use of the standard header will need to be approved by Andover Communications.

* Andover Header: <a href="/html/default__module__andover--header.html">HTML</a>, <a href="/kit/partials/default__module__andover--header.kit">KIT</a>
* Alumni + Giving Header: <a href="/html/default__module__alumni-giving--header.html">HTML</a>, <a href="/kit/partials/default__module__alumni-giving--header.kit">KIT</a>



#### Andover Footer
The standard Andover footer should appear on all templates. The Andover branding logo, whether seal and wordmark or wordmark only, should not resize smaller on a mobile device. The footer copyright, org name and address, and org URL, must use the standard serif font stack. Any template without the standard footer will need to be approved by Andover Communications.

##### Social Media Icons
The standard social media icons should appear on all templates. The standard social media icons for Phillips Academy are:
* Facebook  (Phillips Academy)
* Twitter (Phillips Academy)
* YouTube (Phillips Academy)
* Smugmug (Phillips Academy)
* Forward to a Friend

The standard social media icons for Alumni Engagement and Giving are:
* Alumni Calendar
* LinkedIn (Phillips Academy)
* Alumni Directory
* Facebook (Alumni Engagement)
* Twitter (Phillips Academy)
* Forward to a Friend

The social media icons can be removed or the background color changed depending on the type of template being developed.These changes will need to be approved by Andover Communications.

* Andover Footer: HTML, KIT
* Alumni Engagement Footer: HTML, KIT
* Admission Footer: HTML, KIT


### Helpful Tools

#### Buttons
https://litmus.com/blog/a-guide-to-bulletproof-buttons-in-email-design

#### Image Compression
For PNG images use this compression tool. I have recently found this tool works great:

https://tinypng.com/


### Learned Email Fixes + Helpful Tips

#### Buttons
With a background image, border buttons should be used. You can not use the bulletproof buttons that use VML in Outlook along with a background image which also uses VML in Outlook.

https://litmus.com/blog/a-guide-to-bulletproof-buttons-in-email-design

Currently, manage preferences button is a bulletproof button, which will need to be changed to a border button when using a background image.

**Border Button Resources:**

Manage Preference Border Button: <a href="/html/module--pa--footer-preferences--border-button.html">HTML</a>, <a href="/kit/partials/module--pa--footer-preferences--border-button.kit">KIT</a>

Border Button: <a href="/html/default__module--border-button.html">HTML</a>, <a href="/kit/partials/default__module--border-button.kit">KIT</a>


#### Tablet body fix
Use width:100% !important; and min-width:100%; on the body tag, so the email does not look cut off on an iPad.

    <body style="width:100% !important;min-width:100%;">

#### Image Height - Outlook 2007-2013
For images to work well, height needs to have a specific numbered height. In a media query, use width:100% !important and height:auto !important; for images to size proportionally on devices.

Example:

    <img href="#" width="100" height="100" class="device__width" />

    @media only screen and (max-width: 640px) {
         .device__width {
              width:100% !important;
              height:auto !important;
         }
    }

#### Border-collapse - Outlook
Outlook adds 1px space to all table td elements. The fix, use border-collapse:collapse; on all td elements.

https://www.campaignmonitor.com/blog/post/3392/1px-borders-padding-on-table-cells-in-outlook-07/
http://www.emailonacid.com/images/blog_images/downloads/2014/wp_outlook.pdf

#### Background Image
Instead of specifying a large image for use in the background, if the image can be created and repeated, use a repeatable image.

#### Specify block spacing - Outlook 2013
Avoid using padding or margin to add row space. I am not referring to padding or margin using on paragraphs, but to rows. Instead, use font-size and line-height in table td to add block spacing. A table td alone will cause larger than expected spacing in Outlook 2013. 

    <td class="responsive" width="640" height="10" style="font-size:10px;line-height:10px;">&nbsp;</td>

Another example is how the social media icons were originally coded using padding. Depending on the email client, the padding was ignored. The solution was to center each social media image inside a larger td to add spacing between each image.