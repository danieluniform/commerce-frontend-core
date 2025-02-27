---
title: Frontend Developer Guide | Commerce Frontend Development
description: Learn how frontend developers customize the Adobe Commerce and Magento Open Source storefront and Admin applications.
---

# Frontend Developer Guide

This document provides instructions for creating and installing custom storefront themes for a application. It describes content rendering process and explains the view layer of the system to the extent required to build a theme efficiently. The document also walks through everyday frontend developer's tasks.

Developing the view part of a custom module and customizing the Admin panel design is out of the scope of this guide.

Frontend developers can use this guide to create custom themes to tailor the storefront for a specific customer.

You can apply these levels of customization to your site, where the levels require different development skills:

*  You can make relatively simple changes to your site using Cascading Style Sheets (CSS) to change colors and the look-and-feel of various interface components, replacing images, and other relatively cosmetic changes. For more advanced styling, familiarity with LESS (Leaner Style Sheets) and XML (Extensible Markup Language) is helpful.

    No structural changes are made to pages—you accept the structure of the site provided by default by modules you load on to your site.

    This can be a good starting point for a site as it requires the least effort and knowledge.

*  A small step beyond changing CSS and images on your site is to make changes to the HTML generated by existing modules.

    This requires rudimentary PHP skills to adjust PHTML template files.

    Although PHP coding is involved, this is typically copying and pasting small fragments of PHP code from existing template files into a new template file with differently structured HTML.

    This can be useful if the existing HTML generated does not have sufficient CSS class names or HTML elements to achieve the presentation change you would like to achieve.

*  The next level of sophistication is to make structural changes to your site by moving functionality between places on a page or to completely different pages.

    This is achieved using the layout engine. No PHP coding is required to make layout changes, but the layout engine is moderately sophisticated.

*  Finally, you can develop new modules to add new custom functionality to your site or to extend the functionality provided by existing or third-party modules.

    This third level of customization is not addressed in this guide.

    See the Developer Guide for details on how to develop new modules.

    This requires PHP programming knowledge in addition to knowledge of all of the preceding areas.

## Frontend development prerequisites

To implement what is discussed in this guide, you need a working installation and the following browser versions installed on your device:

Storefront and Admin:

*  Microsoft Edge, latest and previous major version
*  Firefox latest, latest and previous major version (any operating system)
*  Chrome latest, latest and previous major version (any operating system)
*  Safari latest, latest and previous major version (Mac OS only)
*  Safari Mobile for iPad 2, iPad Mini, iPad with Retina Display (iOS 12 or later), for desktop storefront
*  Safari Mobile for iPhone 6 or later; iOS 12 or later, for mobile storefront
*  Chrome for mobile, latest and previous major version (Android 4 or later) for mobile storefront

To use this guide, you must be familiar with:

*  CSS, CSS 3
*  LESS
*  HTML and HTML 5
*  XML
*  JavaScript
*  PHTML
*  PHP (Basic)
*  [Responsive Web Design (RWD)](responsive-design/index.md)
