# selenium-shutterbug

[![Build Status](https://travis-ci.org/assertthat/selenium-shutterbug.svg?branch=master)](https://travis-ci.org/assertthat/selenium-shutterbug)

## Synopsis

Selenium Shutterbug is a utility library make screenshots using [Selenium WebDriver](http://www.seleniumhq.org/projects/webdriver/ "SeleniumHQ WebDriver page") and further customize, compare and process them with the help of  [Java AWT](https://en.wikipedia.org/wiki/Abstract_Window_Toolkit "AWT wiki").

## Code Example

Screenshot of the page, saving to default location (./screenshots/):
````
Shutterbug.shootPage(driver).save();
```
Screenhot of the page with scrolling (for chrome to make screenshot of the whole page but not viewport only):
```
Shutterbug.shootPage(driver, ScrollStrategy.BOTH_DIRECTIONS).save("C:\\testing\\screenshots\\");
```
Screenshotof the single element:
```
Shutterbug.shootElement(driver,element).save("C:\\testing\\screenshots\\");
```

Highlighting, adding titles, text, etc:
```
Shutterbug.shootPage(driver, ScrollStrategy.BOTH_DIRECTIONS)
                .highlight(element)
                .blur()
                .highlightWithText(otherElement, "This is element I was searching for")
                .monochrome()
                .withTitle("Home page screensho")
                .withName("home_page")
                .withThumbnail(0.4).save("C:\\testing\\screenshots\\");
```

And much more...

## Motivation

The idea behing the project is to make testers life easier by enabling them to create descriptive screenshots which, in some cases, could be directly attached to the bug reports or serve as a source of information about system state at a specific time. 

## Installation

The project is available in [Maven Central](http://search.maven.org/#search%7Cga%7C1%7Ca%3A%22selenium-shutterbug%22 "Maven Central project location")

#####Maven dependency

```xml
<dependency>
    <groupId>com.assertthat</groupId>
    <artifactId>selenium-shutterbug</artifactId>
    <version>x.x</version>
</dependency>
```
#####Using Gradle

```
compile 'com.assertthat:selenium-shutterbug:x.x'
```

## License

 Code released under the [MIT license](https://github.com/assertthat/selenium-shutterbug/blob/master/LICENSE "MIT license")
