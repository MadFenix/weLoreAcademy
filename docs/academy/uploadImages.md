# Complete Report on ImgBB and imgbox
*(to upload images and embed them on any website without using its own server)*

---

## Introduction
This report is specifically aimed at the need to **upload images to an external service and embed them (hotlink) on any website**, without using that website’s own storage.  
Two services are analyzed: **ImgBB** and **imgbox**, including free and paid plans, supported formats, limits, API, upload process, and terms of use.

---

# ImgBB (ibb.co / imgbb.com)

## What it is and what it’s for
ImgBB is an image host focused on sharing with **direct links** and embed codes (HTML/BBCode).  
It allows:
- Drag-and-drop upload.
- Paste from clipboard.
- Upload by URL.

Optionally, it offers **auto delete** and provides **ready-to-use embed codes**.

## Formats, size, and key features
- **Formats**: JPG, PNG, BMP, GIF, TIF, WEBP, **HEIC**, **AVIF**, even **PDF**.
- **File limit (free)**: **32 MB**.
- **Embed codes**: viewer link, **linked HTML**, HTML thumbnails, **BBCode**.
- **Album privacy**: Public, private with link, or **private with password**.
- **Auto delete**: from 5 minutes up to 6 months when uploading.

## Plans and pricing
- **Pro Monthly**: $12.99/month
- **Pro Annual**: $7.99/month ($95.88)
- **Pro 3-Year**: $3.99/month ($143.64)

**Pro Advantages**:
- No ads.
- **Direct Linking** (guaranteed).
- Unlimited storage.
- **Replace image**.
- **64 MB** per image.
- **API access**.

> Note: although in practice the free plan already provides direct links, the Pro plan formally guarantees them and adds advanced features.

## How to upload and get an embed link
1. Go to **Upload** and drag the image (or paste/URL).
2. (Optional) Configure **Auto delete** and/or resize.
3. After uploading, copy one of the **Embed codes**:
    - **HTML full linked** → for `<img src="…">`.
    - **BBCode** → forums.
    - Or the **Direct image link**.

Example in HTML:
```html
<img src="https://i.ibb.co/XXXX/myimage.jpg" alt="Description">
```

# imgbox (imgbox.com)

## What it is and what it’s for
imgbox is a **free** and very simple service for hosting and **directly linking** images.  
The homepage shows its basic limits and that it operates under **SSL**.

---

## Formats, size, and key features
- **Formats**: JPG, GIF, and PNG.
- **File limit**: 10 MB.
- **Storage**: “lifetime” (no expiration) as long as the TOS are not violated.
- **Hotlink/bandwidth**: no hard limit; abusive referers may be blocked.

---

## Plans and pricing
- Only a **free** plan exists.
- No paid plans are offered.

---

## How to upload and get an embed link
1. Go to **UPLOAD IMAGES** and drag/select files.
2. After uploading, open the image in full size.
3. Copy the **Direct URL** (ends in `.jpg`, `.png`, or `.gif`) and use it in HTML/Markdown:

```html
<img src="https://images#.imgbox.com/path/file.jpg" alt="Description">
```

## Terms and restrictions
- Hotlink allowed with no “hard” traffic limit.
- The service may block abusive consumption.
- Service provided “as is” and reserves the right to remove illegal/abusive content.

---

## Quick comparison

| Aspect              | ImgBB                                          | imgbox            |
|---------------------|-----------------------------------------------|-------------------|
| **Free / Paid**     | Free; Pro from $3.99–12.99/month              | Free only         |
| **Per image limit** | 32 MB (free) / 64 MB (Pro)                    | 10 MB             |
| **Formats**         | JPG/PNG/GIF/BMP/TIF/WEBP/HEIC/AVIF/PDF        | JPG/PNG/GIF       |
| **Hotlink**         | Direct links and codes; no public quota (abuse may be mitigated) | No hard limit; abusive referers blocked |
| **Privacy/Albums**  | Public, private, password                     | No profiles       |

---

## Practical recommendations
- **For posts with images ≤10 MB and maximum simplicity**: use **imgbox**.  
  Its “no hard limit” bandwidth policy makes it ideal for stable hotlinking (as long as there’s no abuse).

- **For heavier images, modern formats (WEBP/AVIF/HEIC), or auto-expiration**: use **ImgBB**.
