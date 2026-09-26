# Hunter Valley Audiology: Website Content Inventory

**Site:** https://hvaudiology.com.au
**Captured:** 26/09/2026
**Purpose:** A reference for rebuilding the site. It covers the sitemap, the sections on each page, the key content and facts, the text on images, the media assets and the problems found on the current site.

> **About the copy:** Headings, labels, CTAs, contact details, prices and other facts are recorded exactly as they appear. Longer body paragraphs are **summarised** so they can be rewritten; they are not copied word for word. If you need the original copy, export it from the WordPress admin (Tools → Export) or the REST API (`/wp-json/wp/v2/pages`, `/posts`, `/service`, `/hearing`).

---

## 1. Business facts (single source of truth)

| Item | Value |
|---|---|
| Business name | Hunter Valley Audiology |
| Tagline(s) | "Hear Better Connect Better!!!" · "Your Mates in Better Hearing – Enhancing Lives" · "Local and Independent Audiologist!" |
| Founder / clinical audiologist | Jaivikas Gowda ("Jai") |
| Founder background | Master's in Audiology and Speech-Language Pathology (2010). Moved to Australia in 2011. More than 13 years in hearing care, including over a decade at corporate companies |
| Clinic 1 (main) | Shop 7, 18 East Mall, Rutherford 2320 |
| Clinic 2 (visiting) | 54 Brook St, Muswellbrook NSW 2333, Australia |
| Mobile / "Call Us" | 0448 187 960 |
| Landline | +61 2 9184 9628. **The header labels it "Fax", but the location cards and booking meta call it "PHONE". This needs clarifying** |
| Email | info@hvaudiology.com.au |
| Facebook | https://www.facebook.com/HunterValleyAudiology/ |
| Instagram | https://www.instagram.com/huntervalleyaudiology/ |
| LinkedIn | Icon on the About page (founder photo) |
| WhatsApp | https://wa.link/q7mn2g (floating button on every page) |
| Online hearing test | https://hearing-screener.beyondhearing.org/IAmu1Y/ (external screener) |
| Online booking | Hearing Health Portal (australia.hearinghealthportal.com) embed. **Currently broken, see §7** |
| Accreditations / logos | Hearing Services Program **Provider**, Australian College of Audiology, Audiology Australia |
| Hearing aid brands shown | Widex, Phonak ("life is on"), Unitron, Signia |
| Service areas targeted (SEO) | Muswellbrook, Maitland, Rutherford, Newcastle |
| Experience claim | "13 years of experience" |

### Pricing (from the Ear Wax Removal page)

| Item | Price |
|---|---|
| Ear microsuction: 30-minute appointment, one or both ears | **$135.00** |
| Pensioner price: registered with the clinic under the Government Hearing Services Program and completed a hearing assessment with them | **$85.00** |
| Note | An appointment fee may apply even if no wax is removed |
| Rebates | No Medicare rebate and no health fund rebate for wax removal in an audiology clinic |

---

## 2. Sitemap

The site is WordPress with the All in One SEO plugin. The XML sitemap index is at `/sitemap.xml`.

```
/                                   Home
├── /about/                         About
├── /services/                      Services (overview of all 9)
│   └── /service/                   (custom post type "service")
│       ├── hearing-test-at-home/
│       ├── hearing-assessment-for-veterans/
│       ├── hearing-assessment-for-occupation/
│       ├── hearing-aid-fitting/
│       ├── ear-plugs/
│       ├── hearing-assessment-for-adults/
│       ├── tinnitus-management/
│       ├── hearing-aids-for-tinnitus/
│       └── ear-wax-removal/
├── Hearing Health (dropdown)       (custom post type "hearing")
│   ├── /hearing/hearing-aid/
│   ├── /hearing/ear-infection/
│   ├── /hearing/anotomy-of-the-ear/     ← "Anatomy" is misspelled in the slug and menu
│   └── /hearing/common-ear-disease/
├── /blog/                          Blog (27 posts, listed in §5)
├── /contact/                       Contact
├── /booking/                       Booking
├── /category/hearing-aids/ , /category/uncategorized/
└── /tag/…  (12 tag archives)
```

### Global navigation

- **Top bar:** Call Us : 0448 187 960 · Fax : +61 2 9184 9628 · info@hvaudiology.com.au · [CLINIC LOCATION ▾] (Rutherford / Muswellbrook) · [ONLINE HEARING]
- **Main menu:** Home · About · Services · Blog · Hearing Health ▾ (Hearing aid, Ear infection, Anotomy of the ear, Common ear disease) · Contact · [BOOKING →]
- **Floating:** WhatsApp button (bottom right) and an animated ear icon

### Global footer

- Logo strip: Hunter Valley Audiology logo, Australian College of Audiology, audiology australia, and the Hearing Services Program PROVIDER badge
- **Navigation:** Home, About Us, Services, Blogs, Booking, Online hearing, Contact
- **Newsletter:** email field + Submit (Contact Form 7). The HTML still contains leftover template links: "Properties", "Sold Properties", "Standard Management Fees" and the line "Get you good opportunity"
- "Copyright © 2026" · "Designed by Webpristine Technologies"

---

## 3. Page-by-page content

### 3.1 Home `/`
**SEO title:** Best Audiologist Clinics in Muswellbrook, Maitland & Newcastle
**Meta description:** Looking for the best audiologist clinics in Muswellbrook, Maitland and Newcastle. We offer expert hearing tests, hearing aids and personalized hearing care.

| # | Section | Content |
|---|---|---|
| 1 | **Hero slider** (3 slides) | Pill label: "Hear Better **Connect Better!!!**". H1: "Experience Exceptional Hearing Care at Hunter Valley Audiology". Sub: "Your Mates in Better Hearing – Enhancing Lives". CTA: **BOOK AN APPOINTMENT** → /booking/ |
| 2 | **About us** | Eyebrow "About us". H2 "Welcome to Hunter Valley Audiology". Summary: the clinic aims to improve quality of life by improving hearing. The team helps with hearing loss, tinnitus and choosing hearing aids, with caring treatment tailored to each person. Image caption card: "Thank you for considering Hunter Valley Audiology for your hearing healthcare needs. Local and Independent Audiologist!" Image: ear with an invisible in-canal hearing aid, in a hexagon frame |
| 3 | **Brand logos** carousel | Widex, Phonak, Unitron, Signia, Widex (duplicate) |
| 4 | **What makes us Different** (3 cards with photos) | **Local and Independent**: a proudly independent clinic focused on its clients and community. **Years of Experience**: 13 years of experience and up-to-date solutions. **Personalised Approach**: takes time to understand each person's hearing issues and tailor solutions |
| 5 | **Not Sure Where To Begin?** | 1. Schedule an appointment with one of our caring audiologists. 2. Follow this simple step and take an online hearing test. 3. Our support doesn't end with your appointment… Side box: dedication to exceptional service and quality of life |
| 6 | **Services**: "Explore Our Comprehensive Hearing Services" (9 cards, image + title + one line) | See §3.4 for the full list with each card's short description |
| 7 | **Your Preferred Hunter Valley Locations** | Two cards, each with a map image, address, phone (+61 2 9184 9628) and email |
| 8 | **Testimonial** | Google Reviews carousel widget (third-party). Visible reviews are 5★ from Susan Coster, Marlie howley and Lauren Coghlan ("2 years ago"). The reviews mention Jai's experience, a comfortable microsuction wax removal and friendly, professional service |
| 9 | **Contact Us / Get In Touch** | Address: Shop 7, 18 East Mall, Rutherford 2320 · Address (Visiting): 54 Brook St, Muswellbrook NSW 2333 · Email · Phone: 0448 187 960 |
| 10 | **Enquiry form** | Heading: "HAVE QUESTIONS? EAGER TO KNOW MORE? FILL OUT THE FORM BELOW AND WE'LL BE IN TOUCH!" Fields: Full Name*, Email*, Telephone/Mobile*, Message, [Submit]. Uses Contact Form 7, reCAPTCHA and Akismet |

### 3.2 About `/about/`
**SEO title:** Hearing Clinics in Muswellbrook, Maitland & Newcastle
**Meta:** Looking for hearing clinics in Muswellbrook, Maitland or Newcastle? We provide ear wax removal, comprehensive hearing tests and high-quality hearing aids.

| Section | Content |
|---|---|
| Hero | H1 "About-us" (hyphenated as shown) |
| Founder story | Eyebrow "Local and Independent Audiologist!". H4 "A Passionate Journey from Corporate to Community-Centric Hearing Care." Summary: the clinic was founded by clinical audiologist **Jaivikas Gowda (Jai)**, who has more than 13 years in hearing care. He earned a Master's in Audiology and Speech-Language Pathology in 2010 and moved to Australia in 2011. After more than a decade in corporate settings, he values personal care. The clinic aims to educate people about hearing and provide patient-centred community care. Founder photo in a circle with Facebook, Instagram and LinkedIn icons |
| **Why Choose Us?** | **Community-Focused Approach**: a local, independent practice that gives a more personal touch than large chains and builds trust with individualised care and hearing aids. **Expert Knowledge and Experience**: Jai's 13 years in audiology and access to current technology mean each client gets the treatment that fits them. **Holistic and Individualised Care**: care goes beyond fitting devices. The clinic learns each client's daily activities, concerns and goals, whether for hearing aids, earplugs, assessments or tinnitus |

### 3.3 Contact `/contact/`
**SEO title:** Contact Us | Ear Cleaning in Muswellbrook & Rutherford
**Meta:** Get in touch with us for professional Ear Cleaning Services in Muswellbrook & Rutherford. Contact us today to schedule your appointment!
Sections: H1 "Contact-us", H2 "Get in touch", and the enquiry form (same fields as Home). The page body has no addresses, map or opening hours.

### 3.4 Services overview `/services/`
**SEO title:** Hearing Services in Muswellbrook, Maitland & Newcastle
**Meta:** Professional hearing services in Muswellbrook, Maitland & Newcastle. Offering hearing tests, hearing aid fitting and expert audiology care to improve your hearing health.
H1 "Services". The H2 reads "Our Advertiser Services", which looks like leftover template text.

| # | Service | Home card line (summary) | Services-page blurb (summary) |
|---|---|---|---|
| 1 | Hearing Test at Home | Full hearing test in the comfort of your home | Clinicians bring diagnostic kits to your home if you can't get to the clinic |
| 2 | Hearing Assessment for Veterans | Assessments through the Hearing Services Program and Department of Veterans Affairs (DVA) | Same, positioned as the high level of care veterans deserve |
| 3 | Hearing Assessment for Occupation | Job-ready assessments for NSW Police, commercial driving and industrial jobs | Assessments that meet employment specifications (NSW Police, commercial driving medicals) |
| 4 | Hearing Aid Fitting | Precise fitting and adjustment for comfort and clarity | Help from choosing the device through to customised follow-up, fitted to your lifestyle |
| 5 | Ear Plugs | Performance, party, work and construction earplugs | ⚠️ The blurb is wrong: it repeats the Adults assessment text |
| 6 | Hearing Assessment for Adults | Diagnostic devices to assess adult hearing problems | ⚠️ No blurb |
| 7 | Tinnitus Management | Active tinnitus management with expert care and advanced devices | Sound therapy and hearing aids to ease ringing and buzzing |
| 8 | Hearing Aids for Tinnitus | Hearing aids that amplify and help ease tinnitus | Hearing aids combined with tinnitus sound therapy |
| 9 | Ear Wax Removal | Safe, professional ear cleaning | Gentle, effective removal with checks before and after the procedure |

### 3.5 Service detail pages `/service/<slug>/`
**Shared layout:** hero banner with title, left sidebar "All Services" (links to all 9), then the main image and body text.

| Page | SEO title | Body content (summary) |
|---|---|---|
| Hearing Test at Home | Hearing Test at Home in Muswellbrook, Maitland & Newcastle | ⚠️ Only one intro sentence, which **ends mid-sentence with "…"**: patient-centred home hearing tests |
| Hearing Assessment for Veterans | Free Hearing Aids For Pensioners & Veterans \| Muswellbrook | Personalised assessments through the Hearing Services Program and DVA, from a team that understands veterans' needs |
| Hearing Assessment for Occupation | Hearing Assessment for Occupation \| Rutherford & Muswellbrook | ⚠️ Truncated with "…": pre-employment assessments for NSW Police, commercial drivers and industrial workers |
| Hearing Aid Fitting | Hearing Aid Fitting Muswellbrook, Maitland & Newcastle | Guides clients through selecting and customising hearing aids, uses current technology, and provides follow-up maintenance and support |
| Ear Plugs | Ear Plugs in Muswellbrook, Maitland & Newcastle | Earplugs for concerts, noisy work and sleep that reduce noise while keeping sound quality |
| Hearing Assessment for Adults | Hearing Assessment for Adults \| Rutherford & Muswellbrook | Current diagnostic equipment, understanding your specific problems, customised solutions |
| Tinnitus Management | Tinnitus Management Services \| Rutherford & Muswellbrook | Relief for ringing and buzzing using hearing aids with tinnitus therapy and calming masking sounds |
| Hearing Aids for Tinnitus | Hearing Aids for Tinnitus \| Rutherford & Muswellbrook | For people with both hearing loss and tinnitus: amplification plus built-in tinnitus sound therapy |
| **Ear Wax Removal** (the most complete page) | Ear Wax Removal in Muswellbrook, Maitland & Newcastle | See below |

**Ear Wax Removal page structure:**
- **Ear Wax Removal with Microsuction:** the clinic uses a microsuction machine, and its audiologists are trained in the technique. It lists benefits of not using water: better outcomes, a complete solution and less unsteadiness.
- **What is Microsuction?** The ear is examined under a microscope, then a low-pressure suction device removes the wax.
- **Why Choose Microsuction?** It is safe, comfortable and mess-free because no liquids are used, is monitored under the microscope, and takes about 30 minutes.
- **Advantages:** Clear Visibility · Mess-Free Process (lower infection risk than syringing or irrigation) · Safety (suitable for perforated eardrums, mastoid cavities and foreign objects)
- **Restrictions:** not performed during an ear infection or ear pain (see your GP first). If you have a cold or flu, wait until you've recovered.
- **Pre-Appointment Recommendations:** use ear drops or spray for 3–4 days beforehand, unless you've had recent ear surgery or an infection. Without drops the wax may not come out, and the fee still applies. Contact the clinic directly for urgent discomfort.
- **Ear Microsuction Fee:** $135 / $85 for pensioners (see §1)
- **Rebates:** no Medicare rebate and no health fund rebate
- Closing CTA to get in touch or book

### 3.6 Hearing Health pages `/hearing/<slug>/`
**Shared layout:** hero banner, left sidebar linking the 4 topics, then an image and article.

| Page | SEO title | Structure & content (summary) |
|---|---|---|
| Hearing aid | Invisible Hearing Aid in Muswellbrook, Maitland & Newcastle | **"Transform Connections and Enhance Daily Life with Hearing Aids"**: hearing aids as a way to connect, not just amplify, and their basic components. Types offered: invisible-in-canal, behind-the-ear, receiver-in-canal, with Bluetooth and rechargeable options. **Care of Hearing Aids**: wipe daily with a soft cloth, brush off wax, carry a case and spare batteries when travelling, and have regular check-ups. **Why Choose Hunter Valley Audiology for Hearing Aids?** Guidance and recommendations to get the most out of your devices |
| Ear infection | Ear Infection Treatment in Muswellbrook, Maitland & Newcastle | Intro: middle-ear infections are most common in children but can happen at any age. **Symptoms of Ear Infections** (list): ear pain · fullness or pressure · difficulty hearing · fever · headaches · dizziness or balance issues · fluid drainage · irritability or trouble sleeping · tugging at the ear. **How Can We Help?** Hearing is tested once a doctor has medically cleared the infection. The clinic works with GPs and ENT specialists. CTA to book |
| Anotomy of the ear | Anatomy Of The Ear \| Hunter Valley Audiology | **The Outer Ear: The Sound Catcher of Your Body** (pinna and ear canal) → **Note** box on ear wax (why it exists; safe removal offered) → **The Middle Ear: Turning Sound into Movement** (malleus, incus, stapes) → **Note** box on Eustachian tubes and ear "popping" → **The Inner Ear: Where Sound Becomes Sensation** (cochlea hair cells, presbycusis, why older people should have regular checks) |
| Common ear disease | Ear Disease Treatment in Muswellbrook, Maitland & Newcastle | **Common Ear Diseases** → **Ear Infections** · **Tinnitus** · **Hearing Loss** (causes include age and noise; comprehensive assessment offered) · **Meniere's Disease** (vertigo, hearing loss and tinnitus; the clinic helps manage symptoms) |

### 3.7 Booking `/booking/`
**SEO title:** Book Online Hearing Tests in Muswellbrook & Maitland
**Meta:** Book hearing tests online in Muswellbrook and Maitland. View available appointment times and schedule your visit instantly with ease. Call us at +61 2 9184 9628
Content: H1 "Booking" plus an embedded Hearing Health Portal booking iframe. ⚠️ The embed is **broken**: the iframe `src` is `about:blank;australia.hearinghealthportal.com`, so the page shows a large empty area.

### 3.8 Blog `/blog/`
A grid of posts. See §5.

---

## 4. Text on images & image inventory

### 4.1 Images that contain text

| Where | Image | Text in image |
|---|---|---|
| Home hero slide 1 | `users/20241001121230_hunter5.webp` | "life sounds beautifully clear" (orange script). This looks like manufacturer campaign artwork, so check the usage rights before reusing it |
| Header / footer logo | `themes/hunter/assets/images/logo/logo.png`, `uploads/2024/08/logo-3.png`, `logo/foter.png` | "Hunter Valley Audiology": triangle with an ear/soundwave mark, red and navy |
| Brand strip | brand logo images | WIDEX · PHONAK "life is on" · unitron. · signia |
| Footer | `uploads/2025/01/hearing-services-program-visual.png` + ACA / Audiology Australia logos | "Hearing Services Program PROVIDER" · "Australian College of Audiology" · "audiology australia" |
| Location cards | Map screenshot images | Google Maps labels around each clinic (e.g. Muswellbrook Library, BIG W Muswellbrook). Replace these with live embedded maps |
| Service card photo (Hearing Test at Home) | tablet photo | A small website screenshot on the tablet (not legible) |

### 4.2 Photography & graphics (no text)

| Use | File (under `/wp-content/uploads/`) | Description |
|---|---|---|
| Hero slide 2 | `users/20241001121250_hunter2.webp` | Looking up a spiral stone well toward the light |
| Hero slide 3 | `users/…_slide3.webp` / `2024/08/20240828071043_slide3-scaled.webp` | Woman with a red scrunchie wearing a behind-the-ear hearing aid |
| Home About | `2024/09/Group-1000006312-2.webp` | Ear with an invisible hearing aid, red tone, in a hexagon frame |
| Different cards | `2024/08/img1-5.webp`, `img2-1-1.webp`, `img3-2.webp` | Group conversation · older man with a tablet · woman holding a tiny hearing aid |
| Services images | `2024/08/service2-3`, `service3-2`, `service4`, `services`, `service6`, `service7`, `service8`, `processed-1`, `2024/10/UH_PicCampaign_VivanteStridePR_Connectivity-1` | Service photos. The "UH_PicCampaign_Vivante…" file is **Unitron campaign imagery** |
| About founder | `2024/08/Professional-Image-1.webp` | Portrait of Jai |
| Page hero banners | `2024/10/hunter4-1.webp`, `hunter4.webp`, `2024/08/WhatsApp-Image-2024-09-19-at-4.58.54-PM-6.webp`, `2024/10/WhatsApp.webp` | Red-tinted ear anatomy illustrations; booking hero with a hand holding an ear model |
| Hearing Health images | `2024/09/ear-infection.webp`, `2024/09/antomy-of-the-ear-1-scaled.webp`, `2024/08/service2-1.webp` | Topic illustrations. The alt text is the placeholder "Description of the image" |
| Decorative | `themes/hunter/assets/images/icon/ear.png`, `1.png`, `line.svg` | Ear outline icons, dots, double-line dividers |

Alt text across the site is mostly generic ("banner", "service1", "brand", "icon", "Description of the image").

---

## 5. Blog posts (27)

| Date | Title | Words | Main sections |
|---|---|---|---|
| 25/03/2026 | Advanced Invisible Hearing Aids in Newcastle for Modern Hearing Care | 830 | What they are · Why choose · Right for you? · Features · Early treatment · FAQ |
| 16/03/2026 | Improve Your Hearing Today with Newcastle's Leading Audiology Services | 788 | Importance of care · Range of solutions · Why HVA · When to check · FAQ |
| 12/02/2026 | Hearing Test at Home in Newcastle \| Book Home Hearing Check | 918 | What it is · Benefits · Who benefits · Appointment process · Standards |
| 10/02/2026 | Professional Hearing Services in Newcastle \| Expert Hearing Care | 828 | Early evaluation · Services · Technology · Individualised care |
| 15/01/2026 | Free Hearing Aids for Pensioners – Access Better Hearing Without the Cost | 642 | Eligibility · Services included · Advantages · Upgrades · Ongoing support |
| 13/01/2026 | Earplugs in Newcastle – Essential Hearing Protection for Everyday Life | 666 | Protection · Uses · Types · Custom · Sleep & travel · Children |
| 22/12/2025 | Advanced Hearing Clinics in Maitland \| Expert Audiology | 536 | Assessments · Hearing aid services · Ear care · Follow-up |
| 20/12/2025 | Hearing Aid Fitting in Maitland \| Personalised Hearing Care | 588 | Professional fitting · Advantages · Technology · Support |
| 02/12/2025 | Invisible Hearing Aids in Muswellbrook – Discreet, Comfortable, and Life-Changing… | 694 | Why popular · Advantages · Who benefits · Fitting & support |
| 24/11/2025 | Free Hearing Aids for Pensioners Improve Hearing Naturally | 571 | Eligibility · Coverage · Types · How to apply |
| 21/10/2025 | Expert Ear Disease Treatment in Muswellbrook – Advanced Care… | 852 | Common diseases · Eardrum/middle ear · Treatment · Prevention · When to seek help |
| 14/10/2025 | Ear Wax and Hearing Aids: Why Regular Checks Matter | 658 | Impact · Build-up · Symptoms · Frequency · Professional removal |
| 06/10/2025 | Expert Ear Infection Treatment in Muswellbrook – Restoring Comfort… | 761 | Causes & types · Symptoms · Diagnosis · Prevention |
| 25/09/2025 | Free Hearing Aids for Pensioners: A Lifeline to Better Hearing at HVA | 470 | Importance · Muswellbrook services · How to get them |
| 25/08/2025 | The Ultimate Guide to Hearing Aids: Enhancing Your Hearing Health | 709 | Why they matter · Latest tech · Choosing · Benefits |
| 25/07/2025 | Hearing Test Checklist: Are Your Ears Trying to Tell You Something? | 604 | Checklist of signs |
| 25/07/2025 | The Role of Hearing Clinics in Early Detection of Hearing Loss | 485 | Early detection · What clinics do · Technology · Prevention |
| 20/06/2025 | Hearing Clinics in Newcastle and Maitland: Expert Audiology Care Near You | 698 | Early diagnosis · Services · Tinnitus & earwax · Accessibility |
| 29/05/2025 | Clear Your Hearing with Safe Ear Wax Removal in Newcastle | 617 | Why professional · Signs · Process · Who needs checks |
| 25/04/2025 | Understanding Hearing Loss: Causes, Symptoms and When to Seek Help | 731 | Causes · Symptoms · When to seek help |
| 25/03/2025 | Why Should Everyone Undergo a Hearing Test? | 611 | 8 numbered reasons |
| 24/02/2025 | Hunter Valley Audiology: Your Trusted Audiologist in Maitland | 698 | Legacy · Evaluations · Technology · Tinnitus |
| 02/01/2025 | Latest Technology Hearing Aids in Maitland… | 1030 | Addressing loss · Latest tech · Tailored solutions |
| 28/10/2024 | Ear Cleaning in Muswellbrook and Rutherford… | 606 | Importance · Procedure · Muswellbrook · Rutherford · Aftercare |
| 03/10/2024 | How Hunter Valley Audiology Addresses Hearing Loss and Ear Health | 629 | (no subheadings) |
| 03/10/2024 | Understanding Hearing Loss and the Role of Hunter Valley Audiology | 614 | (no subheadings) |
| 29/08/2024 | When Should I Update My Hearing Aids? | 720 | Stopped working · New tech · Hearing changed · Life changes · Weight change |

**Categories:** Hearing Aids (1 post), Uncategorized (26 posts).
**Tags:** Best hearing services · hearing services · Hearing services in Newcastle · Hearing Test in Maitland · Hearing Test in Muswellbrook · Hearing Clinics in Newcastle and Maitland · Ear Wax Removal in Maitland / Muswellbrook / Newcastle / Rutherford · Invisible Hearing Aids · Invisible Hearing Aids in Newcastle. There is also one malformed tag that combines three names.
Most posts are local-SEO articles built around suburb keywords.

---

## 6. Forms, integrations & tech stack

| Item | Detail |
|---|---|
| CMS | WordPress, custom theme "hunter" by Webpristine Technologies |
| Custom post types | `service`, `hearing` |
| SEO | All in One SEO v5 (sitemaps, meta) |
| Forms | Contact Form 7: **Enquiry** (Full Name*, Email*, Telephone/Mobile*, Message) and **Newsletter** (Email*). Protected by Google reCAPTCHA and Akismet |
| Front-end libraries | Bootstrap 5.0.2, jQuery 3.7.1, Owl Carousel 2.3.4 (sliders), AOS (scroll animations), Ionicons |
| Analytics | Google Tag Manager / gtag |
| Third-party | Google Reviews widget · Hearing Health Portal booking · Beyond Hearing online screener · WhatsApp (wa.link) |
| Image optimisation | A plugin serving `.bv.webp` copies under `/wp-content/uploads/al_opt_content/` |

---

## 7. Problems to fix in the rebuild

1. **Booking page is blank.** The Hearing Health Portal iframe URL is malformed.
2. **Service pages are truncated.** Hearing Test at Home and Hearing Assessment for Occupation end in "…", and most service pages are one paragraph long. Only Ear Wax Removal is complete.
3. **Services page copy errors.** The heading reads "Our Advertiser Services". The Ear Plugs blurb duplicates the Adults text, and the Adults blurb is empty.
4. **Phone number confusion.** +61 2 9184 9628 is labelled "Fax" in the header but "Phone" elsewhere. Pick one primary number and label them consistently.
5. **Leftover template content** in the footer: Properties, Sold Properties, Standard Management Fees, and "Get you good opportunity".
6. **Typos:** "Anotomy" appears in the menu, H1 and URL. The H1s are hyphenated as "About-us" and "Contact-us". "Musselbrook" appears in a blog heading.
7. **Duplicate Widex logo** in the brand carousel.
8. **Contact page is thin.** It has no addresses, map, opening hours or phone numbers.
9. **No opening hours** anywhere on the site.
10. **No team page.** Only the founder is mentioned, although the copy refers to "our team".
11. **Map images are screenshots.** Replace them with embedded maps or links to the Google Business Profile.
12. **SEO targets Newcastle and Maitland**, but the only clinics are in Rutherford and Muswellbrook. Consider a service-area page that makes this clear.
13. **Alt text is generic or placeholder** on almost every image.
14. **Blog taxonomy:** 26 of 27 posts are "Uncategorized", and one tag is malformed.
15. **Image rights:** the hero slide 1 artwork and "UH_PicCampaign_Vivante…" appear to be Unitron marketing assets. Confirm the licence before reusing them.
