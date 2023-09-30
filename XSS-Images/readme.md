# XSS in SVG Images in Nabu 1.0

**Software link**: Nabu 1.0 [https://github.com/ricardogj08/nabu]

**@author**: Daniel Puente

**@description**: Cross-site scripting (XSS) vulnerability in SVG images,  an attacker could potentially upload a crafted SVG file and link it making it into an XSS attack.

---
# PoC

1. Crafted SVG file as an XSS-PoC

![image](https://github.com/dd3x3r/XSS-Nabu/assets/74184545/77fbff42-2e6c-4977-bd50-8b84efb93e3f)

2. Upload the image into the CMS, as the profile cover picture (1) or as the profile picture of the user (2).

![image](https://github.com/dd3x3r/XSS-Nabu/assets/74184545/ff6dda63-2779-4895-9246-f438754fcb59)


3. With the picture saved (in the PoC as the profile picture), inspect and copy the link of the source image.

![image](https://github.com/dd3x3r/XSS-Nabu/assets/74184545/65036b46-ad69-4617-9057-2af0ad24a6e6)


4. Create a post with a link to the SVG upoad file.

![image](https://github.com/dd3x3r/XSS-Nabu/assets/74184545/8834ec55-b56d-477b-b84f-e526333148b2)


5. When posted, if clicked it will execute the crafted paylaod.

![image](https://github.com/dd3x3r/XSS-Nabu/assets/74184545/d4525f55-6ab4-4bab-afe6-aac2d18ba8ac)
![image](https://github.com/dd3x3r/XSS-Nabu/assets/74184545/e8a18003-51f7-4490-8aaf-9348698999b2)


