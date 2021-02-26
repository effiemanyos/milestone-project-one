# **TESTING**

## **Issues Solved During Development**
-----

- ONE

- TWO

- THREE

- FOUR

- FIVE

- SIX

- SEVEN

- EIGHT

- NINE

- TEN

## **HTML/CSS Validation Testing**
-----

### **1. HTML Validation**

The tool used for this code validation was the [W3C Markup Validation Service](https://validator.w3.org/), which was used by **Direct Input** to make sure there were no erros in the **HTML File**. The results were the following:

![w3c html validation service one error results](./assets/images/html-initial-validation.png "w3c css validation service one error results") 

***Date:*** Thursday, Feb 25th, 2021

- **Issue:** Bad value "mailto: effie@gmail.com" for attribute `href` on element `a`: Illegal character in scheme data: **space is not allowed**.

- **Fixes:** All the extra spaces were removed resulting in:

```HTML
<p><a href="mailto:effie@gmail.com">effie@gmail.com</a></p>
```

The final report shows no errors in the index.html file as they were properly fixed:

![w3c html validation service one error results](./assets/images/html-final-validation.png "w3c css validation service one error results") 

***Date:*** Thursday, Feb 25th, 2021

### **2. CSS Validation**

The tool used for this code validation was the [W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/), which was used by **Direct Input** to make sure there were no erros in the **CSS Style Sheet**. The results were the following:

![w3c css validation service no error results](./assets/images/css-validation.png "w3c css validation service no error results") 

***Date:*** Thursday, Feb 25th, 2021

The CSS yielded no errors, so I proceeded with further testing. However, it is worth noting that I also got these five warning results to be considered:

![w3c css validation service warning results](./assets/images/css-warnings.png "w3c css validation service warning results") 

Just in case, I redid the testing by **File Upload** and the results were exactly the same. 

## **Testing Performance**
-----

### **1. Desktop**

In order to test the website's performance on desktop and mobile, [Google Lighthouse](https://developers.google.com/web/tools/lighthouse) was used. The results were the following:

![google lighthouse desktop results](./assets/images/lighthouse-desktop-p1.png "google lighthouse desktop results") 

![google lighthouse desktop results](./assets/images/lighthouse-desktop-p2.png "google lighthouse desktop results") 

![google lighthouse desktop accessibility results](./assets/images/lighthouse-desktop-accessibility.png "google lighthouse desktop accessibility results") 

***Date:*** Thursday, Feb 25th, 2021

**Urgent Issues:**

- **Issue:** Remove unused JavaScript

- **Fixes:**

- **Issue:** Properly size images

- **Fixes:**

- **Issue:** Eliminate render-blocking resources

- **Fixes:**

- **Issue:** Avoid enourmous network payloads

- **Fixes:**

- **Issue:** Image elements do not have explicit widh and height

- **Fixes:**

- **Issue:** Ensure text ramains visible during webfont load

- **Fixes:**

- **Issue:** Form elements do not have associated labels

- **Fixes:**

- **Issue:** Links do not have a discernible name

- **Fixes:**

## **Testing User Stories**
-----



## **Testing Accessibility**
-----