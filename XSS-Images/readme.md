# XSS in SVG Images in Nabu 1.0

**Software link**: Nabu 1.0 [https://github.com/ricardogj08/nabu]

**@author**: Daniel Puente

**@description**: Cross-site scripting (XSS) vulnerability in SVG images,  an attacker could potentially upload a crafted SVG file and link it making it into an XSS attack.

---
# PoC

1. Crafted SVG file as an XSS-PoC

![image](https://github.com/dd3x3r/XSS-Nabu/assets/74184545/92eda9f8-42dd-48ba-b1ff-2d4a53245d88)

2. Upload the image into the CMS, as the profile cover picture (1) or as the profile picture of the user (2).

![image](https://github.com/dd3x3r/XSS-Nabu/assets/74184545/a51f4538-c84f-4abe-8e6b-df41c421c55b)

3. With the picture saved (in the PoC as the profile picture), inspect and copy the link of the source image.

![image](https://github.com/dd3x3r/XSS-Nabu/assets/74184545/d3d79ff5-7af4-4e2c-b5b9-f310562b5b32)


4. Create a post with a link to the SVG upoad file.

![image](https://github.com/dd3x3r/XSS-Nabu/assets/74184545/16eb677e-8df3-468e-b697-55be61d44d7e)

5. When posted, if clicked it will execute the crafted paylaod.

![image](https://github.com/dd3x3r/XSS-Nabu/assets/74184545/1f5fb2ed-5586-4a97-b2da-0e3681a8f318)
![image](https://github.com/dd3x3r/XSS-Nabu/assets/74184545/05443b51-c261-4fd2-a302-c10b619e8dfe)

