# **Testing**

## **Issues Solved During Development**

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

## **Testing User Stories**

## **Testing Performance**

## **Testing Accessibility**
