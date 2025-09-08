<h1 align="center">CSS Notes</h1>

### 0.1. Table of Contents
- [1. CSS Introduction](#1-css-introduction)
  - [1.1. How To Add CSS](#11-how-to-add-css)
  - [1.2. CSS Comments](#12-css-comments)
- [2. variables](#2-variables)
- [3. Cascading order, Specificity](#3-cascading-order-specificity)
  - [3.1. Cascading Order](#31-cascading-order)
  - [3.2. Specificity](#32-specificity)
- [4. CSS Text Formatting](#4-css-text-formatting)
  - [4.1. text-color](#41-text-color)
  - [4.2. text-alignment](#42-text-alignment)
  - [4.3. text-direction:](#43-text-direction)
  - [4.4. text-decoration:](#44-text-decoration)
  - [4.5. Text-transformation:](#45-text-transformation)
  - [4.6. letter-spacing:](#46-letter-spacing)
  - [4.7. word-spacing:](#47-word-spacing)
  - [4.8. line-height:](#48-line-height)
  - [4.9. text-shadow:](#49-text-shadow)
  - [4.10. font-size:](#410-font-size)
  - [4.11. font-weight:](#411-font-weight)
- [5. CSS Margin](#5-css-margin)
  - [5.1. The auto value](#51-the-auto-value)
  - [5.2. Margin Collapse](#52-margin-collapse)
- [6. CSS Border](#6-css-border)
  - [6.1. border](#61-border)
- [7. CSS Padding](#7-css-padding)
- [8. CSS Box-Modal](#8-css-box-modal)
  - [8.1. CSS Box-sizing](#81-css-box-sizing)
    - [8.1.1. box-sizing: content-box(default)](#811-box-sizing-content-boxdefault)
    - [8.1.2. box-sizing: border-box](#812-box-sizing-border-box)
- [9. CSS Background Properties](#9-css-background-properties)
  - [9.1. Multiple Backgrounds images](#91-multiple-backgrounds-images)
- [10. CSS Units](#10-css-units)
- [11. CSS Selectors](#11-css-selectors)
  - [11.1. Simple Selectors](#111-simple-selectors)
    - [11.1.1. Element Selector](#1111-element-selector)
    - [11.1.2. Id Selector](#1112-id-selector)
    - [11.1.3. Class Selector](#1113-class-selector)
    - [11.1.4. Universal Selector](#1114-universal-selector)
    - [11.1.5. Groping Selector](#1115-groping-selector)
  - [11.2. Combinator Selectors](#112-combinator-selectors)
  - [11.3. Pseudo-class Selectors](#113-pseudo-class-selectors)
    - [11.3.1. Pseudo-classes with links](#1131-pseudo-classes-with-links)
      - [11.3.1.1. simple tooltip hover](#11311-simple-tooltip-hover)
    - [11.3.2. input:focus](#1132-inputfocus)
    - [11.3.3. :nth-child()](#1133-nth-child)
- [12. CSS Table](#12-css-table)
  - [12.1. Table Borders:](#121-table-borders)
  - [12.2. Collapsed Table Border:](#122-collapsed-table-border)
  - [12.3. Style Table Borders:](#123-style-table-borders)
  - [12.4. Round Table Borders:](#124-round-table-borders)
  - [12.5. Text-Align:](#125-text-align)
  - [12.6. Vertical-align:](#126-vertical-align)
  - [12.7. Dotted Table Borders:](#127-dotted-table-borders)
  - [12.8. HTML Table Width:](#128-html-table-width)
  - [12.9. HTML Table height:](#129-html-table-height)
  - [12.10. Vertical Table Headers:](#1210-vertical-table-headers)
  - [12.11. Align Table Headers:](#1211-align-table-headers)
  - [12.12. Cell padding:](#1212-cell-padding)
  - [12.13. Cell Spacing:](#1213-cell-spacing)
  - [12.14. HTML Table -Colspan:](#1214-html-table--colspan)
  - [12.15. HTML Table- Rowspan:](#1215-html-table--rowspan)
  - [12.16. HTML Table – Zebra Stripes:](#1216-html-table--zebra-stripes)
  - [12.17. HTML Table – Vertical Zebra Stripes:](#1217-html-table--vertical-zebra-stripes)
  - [12.18. Combine Vertical and Horizontal Zebra Stripes:](#1218-combine-vertical-and-horizontal-zebra-stripes)
  - [12.19. Horizontal Dividers:](#1219-horizontal-dividers)
  - [12.20. Hover able Table:](#1220-hover-able-table)
- [13. Display Property](#13-display-property)
- [14. Position Property](#14-position-property)
  - [14.1. static(default):](#141-staticdefault)
  - [14.2. Relative:](#142-relative)
  - [14.3. absolute:](#143-absolute)
  - [14.4. Sticky:](#144-sticky)
  - [14.5. Fixed:](#145-fixed)
- [15. z-index property](#15-z-index-property)
- [16. Overflow](#16-overflow)
- [17. Opacity](#17-opacity)
- [18. Box shadow](#18-box-shadow)
  - [18.1. Specify a Horizontal and a Vertical shadow:](#181-specify-a-horizontal-and-a-vertical-shadow)
  - [18.2. Specify a color for the shadow:](#182-specify-a-color-for-the-shadow)
  - [18.3. Add a blur effect to the shadow:](#183-add-a-blur-effect-to-the-shadow)
  - [18.4. Set the spread radius of the shadow:](#184-set-the-spread-radius-of-the-shadow)
  - [18.5. Set the inset parameter:](#185-set-the-inset-parameter)
- [19. Media Queries](#19-media-queries)
  - [19.1. CSS Media Types:](#191-css-media-types)
  - [19.2. CSS Media Features:](#192-css-media-features)
  - [19.3. Syntax:](#193-syntax)
  - [19.4. Fully responsive media queries breakpoints:](#194-fully-responsive-media-queries-breakpoints)





## 1. CSS Introduction
CSS = Cascading Style Sheets

It is a stylesheet language used to describe the presentation of a document written in HTML. CSS controls the layout, design, and visual presentation of web pages.

![css-syntax](./assets/images/css-syntax.png)

- The selector pints to the HTML element you want to style.
- The Declaration block contains one or more declarations separated by semicolons and surrounded by curly braces.  Each Declaration includes a CSS property name and a value, separated by a colon.

### 1.1. How To Add CSS

 There are three ways of inserting a style sheet:

1. Inline CSS
   
```<h1 style="color: red;">Inline CSS</h1>```

2. Internal CSS
```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        h1{
            color: red;
        }
    </style>
</head>
```
3. External CSS
```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
```
```css
h1{
    color: red;
}
```

### 1.2. CSS Comments
```css
/* This is a single line comments */

/* This is 
a multi-line
comment */
```

## 2. variables
A CSS variable (also called a custom property) is a reusable value that you define once and use multiple times in your CSS. CSS variables are usually defined inside the :root selector so that they are available globally.

```css
:root{
    --main-color: blue:
    --main-font: 20px; 
}

body{
    background-color: var(--main-color);
    font-size: var(--main-font);
}
```

## 3. Cascading order, Specificity
### 3.1. Cascading Order 
### 3.2. Specificity


## 4. CSS Text Formatting
### 4.1. text-color
### 4.2. text-alignment
### 4.3. text-direction:	
### 4.4. text-decoration:	
### 4.5. Text-transformation:	
### 4.6. letter-spacing:	
### 4.7. word-spacing:	
### 4.8. line-height:	
### 4.9. text-shadow:	
### 4.10. font-size:	
### 4.11. font-weight:

## 5. CSS Margin
### 5.1. The auto value
### 5.2. Margin Collapse

## 6. CSS Border
### 6.1. border

## 7. CSS Padding

## 8. CSS Box-Modal
### 8.1. CSS Box-sizing
#### 8.1.1. box-sizing: content-box(default) 
#### 8.1.2. box-sizing: border-box 

## 9. CSS Background Properties
### 9.1. Multiple Backgrounds images

## 10. CSS Units

## 11. CSS Selectors
### 11.1. Simple Selectors
#### 11.1.1. Element Selector
#### 11.1.2. Id Selector
#### 11.1.3. Class Selector
#### 11.1.4. Universal Selector
#### 11.1.5. Groping Selector
### 11.2. Combinator Selectors
### 11.3. Pseudo-class Selectors
#### 11.3.1. Pseudo-classes with links
##### 11.3.1.1. simple tooltip hover
#### 11.3.2. input:focus
#### 11.3.3. :nth-child()


## 12. CSS Table
### 12.1. Table Borders:	
### 12.2. Collapsed Table Border:	
### 12.3. Style Table Borders:	
### 12.4. Round Table Borders:	
### 12.5. Text-Align:	
### 12.6. Vertical-align:	
### 12.7. Dotted Table Borders:	
### 12.8. HTML Table Width:	
### 12.9. HTML Table height:	
### 12.10. Vertical Table Headers:	
### 12.11. Align Table Headers:	
### 12.12. Cell padding:	
### 12.13. Cell Spacing:	
### 12.14. HTML Table -Colspan:	
### 12.15. HTML Table- Rowspan:	
### 12.16. HTML Table – Zebra Stripes:	
### 12.17. HTML Table – Vertical Zebra Stripes:	
### 12.18. Combine Vertical and Horizontal Zebra Stripes:	
### 12.19. Horizontal Dividers:	
### 12.20. Hover able Table:


## 13. Display Property

## 14. Position Property
### 14.1. static(default):
### 14.2. Relative:	
### 14.3. absolute:	
### 14.4. Sticky:	
### 14.5. Fixed:	


## 15. z-index property

## 16. Overflow

## 17. Opacity

## 18. Box shadow
### 18.1. Specify a Horizontal and a Vertical shadow:	
### 18.2. Specify a color for the shadow:	
### 18.3. Add a blur effect to the shadow:	
### 18.4. Set the spread radius of the shadow:	
### 18.5. Set the inset parameter:	


## 19. Media Queries
### 19.1. CSS Media Types:	
### 19.2. CSS Media Features:	
### 19.3. Syntax:	
### 19.4. Fully responsive media queries breakpoints:


