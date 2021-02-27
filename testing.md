# **Content** 

- [Testing](#testing "Testing")
  - [Issues Solved During Development](#issues-solved-during-development "Issues Solved During Development")
  - [HTML-CSS Validation Testing](#html-css-validation-testing "HTML-CSS Validation Testing")
  - [Testing Performance](#testing-performance "Testing Performance")
  - [Testing Accessibility](#testing-accessibility "Testing Accessibility")
  - [Testing User Stories](#testing-user-stories "Testing User Stories")
  - [Code Institute Peer Code Review](#code-institute-peer-code-review "Code Institute Peer Code Review")

  [Return to README.md Document](https://github.com/effiemanyos/milestone-project-one/blob/master/README.md)

# **TESTING**

![the webpage on different devices](./assets/images/mockup-img.png "the webpage on different devices")

The website was tested in the following **browsers**:

- Chrome √
- Firefox √
- Microsoft Edge √
- Safari √
- Internet Explorer X
- Opera √

It was also tested in the following phone **operating systems**:

- iOS √
- Android √

Finally, it was tested in the following **devices**:

- Desktop √
- iPhone 5/SE √
- Pixel 2/2XL √
- Moto 4G √
- Galaxy S5 √
- iPhone 6/7/8 (+Plus) √
- iPhone X/iPhone XS Max √
- iPad/iPad Pro √
- Surface Duo √

*Results:* 

The website had an great performance and could be used perfectly, no funcional issues were found during the testing. However, the layout was not exactly the same (or the intended design) in all systems and devices but the users could interact with ease and achieve their goals successfully.

## **Issues Solved During Development**
-----

The most important issues that were found during development that took a considered amount to time to solve are the following:

- ONE

- TWO

- THREE

- FOUR

- FIVE

[Back to Content](#content)

## **HTML-CSS Validation Testing**
-----

### **1. HTML Validation**

The tool used for this code validation was the [W3C Markup Validation Service](https://validator.w3.org/), which was used by **Direct Input** to make sure there were no erros in the **HTML File**. The results were the following:

![w3c html validation service one error results](./assets/images/html-initial-validation.png "w3c css validation service one error results") 

***Date:*** Thursday, Feb 25th, 2021

**1. Issue:** Bad value "mailto: effie@gmail.com" for attribute `href` on element `a`: Illegal character in scheme data: **space is not allowed**.

- **Fixes:** All the extra spaces were removed resulting in:

```HTML
<p><a href="mailto:effie@gmail.com">effie@gmail.com</a></p>
```

The **final report** shows no errors in the index.html file as they were properly fixed:

![w3c html validation service one error results](./assets/images/html-final-validation.png "w3c css validation service one error results") 

***Date:*** Thursday, Feb 25th, 2021

### **2. CSS Validation**

The tool used for this code validation was the [W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/), which was used by **Direct Input** to make sure there were no erros in the **CSS Style Sheet**. The results were the following:

![w3c css validation service no error results](./assets/images/css-validation.png "w3c css validation service no error results") 

***Date:*** Thursday, Feb 25th, 2021

The CSS yielded no errors, so I proceeded with further testing. However, it is worth noting that I also got these five warning results to be considered:

![w3c css validation service warning results](./assets/images/css-warnings.png "w3c css validation service warning results") 

Just in case, the testing was done again, this time by **File Upload**, and the results were exactly the same. 

## **Testing Performance**
-----

In order to test the website's performance on **desktop** and **mobile**, [Google Lighthouse](https://developers.google.com/web/tools/lighthouse) was used in both cases.

### **Desktop & Mobile**

The **initial results** were the following:

![google lighthouse results](./assets/images/lighthouse-p1.png "google lighthouse results") 

![google lighthouse results](./assets/images/lighthouse-p2.png "google lighthouse results") 

![google lighthouse accessibility results](./assets/images/lighthouse-accessibility.png "google lighthouse accessibility results") 

![google lighthouse best practices results](./assets/images/lighthouse-bestpractices.png "google lighthouse best practices results") 

![google lighthouse runtime settings](./assets/images/runtime-settings.png "google lighthouse runtime settings") 

***Date:*** Thursday, Feb 25th, 2021

The following actions were taken to improve the performance of the website, especially the accessibility:

**Urgent Issues:**

**1. Issue:** Properly size images / Avoid enourmous network payloads

- **Fixes:** Unfortunatly, due to the lack of time this issue could not be solved before the project deadline. However, all the images used on the website will be converted from PNG to formats like JPEG 2000 or WebP to provide better compression for faster downloads and less data consumption. The tools that will be used for this are the following: [Convertio (PNG to WebP)](https://convertio.co/png-webp/) and [TinyPNG (Image Compression)](https://tinypng.com/). **Goal:** Less than 550KB per image.

**2. Issue:** Links to cross-origin destinations are unsafe

- **Fixes:** This issue was simply fixed by adding `rel="noopener"` to all external links to prevent security vulnerabilities.

```HTML
<li>
    <img src="assets/images/ah-logo.png" alt="ArchHyve logo">
    <a href="https://archhyve.com/" target="_blank" rel="noopener"><img src="assets/images/ah-img.png" alt="ArchHyve"></a>
</li>
```

**3. Issue:** Image elements do not have explicit widh and height

- **Fixes:** Unfortunatly, due to the lack of time this issue could not be solved before the project deadline. However, explicit `width` and `height` (size attributes) will be set on image and video elements to reduce layout shifts and improve CLS (Cumulative Layout Shift) like explained in [Optimize Cumulative Layout Shift](https://web.dev/optimize-cls/?utm_source=lighthouse&utm_medium=devtools#images-without-dimensions).

*Example:*
```HTML
<img src="community-logo.jpg" width="640" height="360" alt="the club community official logo"/>
```

**4. Issue:** Background and foreground colors do not have a sufficient contrast ratio √

- **Fixes:** This issue was simply fixed by increasing the contrast of the colors in the background and foreground.

```CSS
#new-bgfg-colors {
    background: #e7e8ef;
    color: #434343;
}
```
*Final Result:*
![background and foreground new colors](./assets/images/increased-contrast.png "background and foreground new colors") 

**5. Issue:** Ensure text ramains visible during webfont load

- **Fixes:**

**6. Issue:** Form elements do not have associated labels

- **Fixes:** This issue was simply fixed by adding the associated labels to all form elements.

```HTML
<!-- Name -->
<label for="fullname">Full Name</label>
<input type="text" name="name" id="fullname" class="form-control" placeholder="Full Name" required/>
```

```CSS
/* Invisible Form Labels */
label {
    display: none;
}
```

*Final Result:*

![background and foreground new colors](./assets/images/form-labels.png "background and foreground new colors")

*Final Results:*

![google lighthouse final results](./assets/images/lighthouse-finalresults.png "google lighthouse final results")

[Back to Content](#content)

## **Testing Accessibility**
-----

To test the website accessibility [Wave Web Accessibility Evaluation Tool](https://wave.webaim.org/) was used. The obtained results are the following:

![wave accessibility results](./assets/images/wave-accessibility-results.png "wave accessibility results") 

![wave accessibility errors and alerts results](./assets/images/wave-accessibility-errorsalerts.png "wave accessibility errors and alerts results")

All "errors" and "alerts" were analysed in detail and the **conclusions** were the following: 

- All the **alerts** were actually made on purpose for academic reasons only as the external links used in the development of this project are not the real ones (e.g.: social media links) or they have been duplicated as the information shared on the site requires:

![wave accessibility alerts results](./assets/images/wave-accessibility-redundantlinks1.png "wave accessibility errors and alerts results")

![wave accessibility alerts results](./assets/images/wave-accessibility-redundantlinks2.png "wave accessibility errors and alerts results")

- All these **errors** on the site are the same, the `<a>` tag doesn't contain any text: 

![wave accessibility errors results](./assets/images/wave-accessibility-errors.png "wave accessibility errors and alerts results")

In order to fix this to improve the accessibility of the website, `alt text` was added to all social media icons so that the text can be detected by screen readers only:

```HTML
<!-- Hidden Text Social Media Icons | SR Only -->
<a href="https://www.linkedin.com/" target="_blank" rel="noopener"><i class="fa fa-linkedin"><span class="sr-only">LinkedIn</span></i></a>
<a href="https://www.facebook.com/" target="_blank" rel="noopener"><i class="fa fa-facebook"><span class="sr-only">Facebook</span></i></a>
<a href="https://www.instagram.com/" target="_blank" rel="noopener"><i class="fa fa-instagram"><span class="sr-only">Instagram</span></i></a>
<a href="https://twitter.com/" target="_blank" rel="noopener"><i class="fa fa-twitter"><span class="sr-only">Twitter</span></i></a>
```

```CSS
/* Hidden Text Social Media Icons | SR Only */
.sr-only {
    font-size: 0;
    height: 1px;
    overflow: hidden;
    display: block;
}
```

> Credit: ["Add Text Alternate to Social Media Icons" by Sylvia Pellicore](https://github.com/girldevelopit/gdi-website/issues/344)

*Final Results:*

![wave accessibwaveility errors results](./assets/images/wave-accessibility-finalresults.png "wave accessibility errors and alerts results")

[Back to Content](#content)

## **Testing User Stories**
-----

![screenshot of the welcome section of the website](./assets/images/welcome-screenshot.png "screenshot of the welcome section of the website")
![screenshot of the about me section of the website](./assets/images/about-screenshot.png "screenshot of the about me section of the website")
![screenshot of the services section of the website](./assets/images/services-screenshot.png "screenshot of the services section of the website")
![screenshot of the testimonials section of the website](./assets/images/testimonials-screenshot.png "screenshot of the testimonials section of the website")
![screenshot of the contact section of the website](./assets/images/contact-screenshot.png "screenshot of the contact section of the website")
![screenshot of the footer section of the website](./assets/images/footer-screenshot.png "screenshot of the footer section of the website")

*Visitor Types:*

1. As a **First Time Visitor**, I want to know **who Effie is** and what she does so that I can evaluate if I need her expertise to scale my business (SMEs)
    > XXXX
2. As a **First Time Visitor**, I want to know what **qualifications** Effie has so that I can use the resources she offers to increase my client base and profit (Entry-Level Professionals)
    > XXXX
3. As a **First Time Visitor**, I want to know what kind of **services** Effie offers so that I can come back whenever I need them to launch my business idea (Entrepreneurs)
    > XXXX
4. As a **First Time Visitor**, I want to know about Effie's **work experience** so that I can get in touch with her once I finish my studies (Recent Graduates)
    > XXXX
5. As a **First Time Visitor**, I want to Know **what other people say about Effie** so that I can hire her to manage my social media accounts (Solopreneurs)
    > XXXX

6. As a **Returning Visitor**, I want to **make sure** Effie's **site is not a scam** so that I can pay for her services before the product launch (Tech Startups)
    > XXXX
7. As a **Returning Visitor**, I want to **contact** Effie so that we can work together on my business growth and retention rates (SMEs)
    > XXXX
8. As a **Returning Visitor**, I want to **book** Effie's **free consultation** so that I can create a solid Digital Marketing strategy for my business (Solopreneurs)
    > XXXX
9. As a **Returning Visitor**, I want to **call Effie directly** so that I can start working with her on my personal branding to get a corporate job in Ireland (Professional Expats)
    > At the moment, the booking (Calendly integration) is not an available feature; however, users can book their free consultations through the Contact Me Form or by Calling Directly. Navigation Bar (Contact), About Me Section (CTA Button), How Can I Help Section (CTA Button), What I Do (CTA Button), Get In Touch Section (Contact Information & Form).
10. As a **Returning Visitor**, I want to **send Effie a message** so that I can be sure that she would be able to work on the product-market fit for my business idea (Recent Graduates)
    > XXXX

As stated in the [README.md](https://github.com/effiemanyos/milestone-project-one/blob/master/README.md) file, the following features required by the **returning visitors** and **key target audience features** will be implemented by the second month after the launch of the MVP.

*Frequent Visitors:*
1. As a **Frequent Visitor**, I want to **register** to Effie's **upcoming online workshops and events** so that I can learn more marketing and business skills for my entrepreurial venue (Recent Graduate)
    > Feature that will be implemented in the next iteration (Training Page: Online Workshops).
2. As a **Frequent Visitor**, I want to **join Effie's community for expats (Huasi)** so that I can meet more connections to land my dream job faster (Professional Expats)
    > Feature that will be implemented in the next iteration (Join Us Page: Join Huasi or Join NetCork Communities).
3. As a **Frequent Visitor**, I want to **pay a monthly or annually subscription** so that I can always be up to date with the latest methods and frameworks for my business growth (Entrepreneurs)
    > Feature that will be implemented in the next iteration (Join Us Page: Membership Plans).
4. As a **Frequent Visitor**, I want to **pay online for Effie's services** so that I can reduce churn and increase product adoption and customer retention (Tech Startups)
    > Feature that will be implemented in the next iteration (Online Payment).
5. As a **Frequent Visitor**, I want to **get the freemium plan** so that I can use Effie's free resources and implement them to growth my business (Solopreneurs)
    > Feature that will be implemented in the next iteration (Join Us Page: Membership Plans).

*Target Audience:*

1. As an **Entrepreneur/Solopreneur**, I want to **register** to Effie's **online workshops** so that I can boost my business' monthly sales.
    > Feature that will be implemented in the next iteration (Training Page: Online Workshops).
2. As a **Tech Startup**, I want to **use** Effie's **free online resources** so that we can create a robust Digital Marketing strategy.
    > Feature that will be implemented in the next iteration (Resources Page: Free Resources).
3. As a **SME**, I want to **book** a **free consultaiton** with Effie so that we can increase our business' online presence and engagement.
    > Feature that will be implemented in the next iteration (Contact Me Page: Calendly Integration).
4. As a **Non-Profit**, I want to **contact** Effie for a **collaboration** and **consulting session** so that we can grow the organization organically.
    > Users can contact Effie through the following: Navigation Bar (Contact), About Me Section (CTA Button), How Can I Help Section (CTA Button), What I Do (CTA Button), Get In Touch Section (Contact Information & Form).
5. As a **Mentee**, I want to **apply** to Effie's **mentorship program** so that I can get the proper guidance to build my professional career.
    > Feature that will be implemented in the next iteration (Services Page: Mentorship Program Applycation).
6. As an **Entry-Level Professional**, I want to **join** Effie's **networking community** so that I can land my first full-time job faster through contacts.
    > Feature that will be implemented in the next iteration (Join Us Page: Join Huasi or Join NetCork Communities).
7. As a **Recent Graduate**, I want to **consume** Effie's **free courses and resources** so that I can launch my business idea.
    > Feature that will be implemented in the next iteration (Training Page: Online Courses & Resources Page: Free Resources).
8. As a **Professional Expat**,I want to **learn** from Effie's successful journey so that I know where to start mine as a new international professional in Ireland.
    > Feature that will be implemented in the next iteration (About Page: Online Video, Effie's Journey).

[Back to Content](#content)

## **Code Institute Peer-Code-Review**
-----

- **Sean McMahon:** "Beautiful design and very consistent. I really like the transitions on the company logos."
- **Francis Kershaw:** "This is so good, Effie! Can tell how hard you've worked on it, well done!"
- **Janelle MacMillan:** "I think this looks great, Effie, and I really can't find anything other than that to say about it."
- **Michael Nota Rita:** "It looks great! 5 stars for me!"

Unfortunatly, there were no constructive feedback to work on in order to improve user experience despite it was requested twice.

- **Cormac Lawlor:** "That's super impressive! Love it. One thing, your images like your hero are massive! It's slowing down your site. Might be worth reducing the file size."

[Back to Content](#content)

[Return to README.md Document](https://github.com/effiemanyos/milestone-project-one/blob/master/README.md)
