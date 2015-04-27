title: FluentConf 2015
author:
  name: Lin Dong
  twitter: _ldong
  <!-- url: https://github.com/ldong/FluentConf2015 -->
  email: ldong@zscaler.com
output: demo.html
controls: true

--

# FluentConf 2015 Notes

## San Francisco, CA

## April 20, 2015

## Lin Dong

--

# Morning Section

## 1. Powering APIs with Go
## -- William Kennedy
## 2. W3C Web Performance APIs in Practice
## -- Alois Reitbauer

--

### Powering APIs with `Go`

1. [Go](https://golang.org/) is very like C just better.
<!-- Golang, is a programming language initially developed at Google in 2007
  by Robert Griesemer, Rob Pike, and Ken Thompson -->

2. [Download](https://github.com/ArdanStudios/gotraining) via `git clone https://github.com/ArdanStudios/gotraining`

3. i.e. [Variables - Language Syntax](https://github.com/ArdanStudios/gotraining/tree/master/01-language_syntax/01-variables)

--

### Go: build-in type

```go
package main
import fmt

func main(){
  var a int
  var b string
  var c float64 // declare and assign to its default value
  var d bool
}

aa := 10
bb := "hello"
cc := 3.1415
dd := false
```

1. `var` will assign it to 0 value

2. `int` is architecture specific.

3. `string` is immutable by default.

---

### 3 take aways

1. Write codes in a way can gain **Mechanical Sympathy**
<!-- Try to write the code that can allow the compilers to help you optimize
the efficency -->

2. Using **logs** more often than debuggers
<!-- There are limits for hotfixing on bugs on production, so writing logs is
more proper, and because Go does not have a builtin debugger for you -->

3. [There is no inheritance in Go](http://nathany.com/good/), i.e.

  1. [StackOverflow](http://stackoverflow.com/questions/1727250/embedding-instead-of-inheritance-in-go)

  2. [Inheritance and subclassing in Go - Blog](http://golangtutorials.blogspot.com/2011/06/inheritance-and-subclassing-in-go-or.html)

<!-- 4. [You Don't Like Google's Go Because You Are Small](http://tmikov.blogspot.com/2015/02/you&#45;dont&#45;like&#45;googles&#45;go&#45;because&#45;you.html) -->

I would advise to read the [doc](https://golang.org/doc/faq) first, and
understand its philosophy before you actually start writting codes.

--

### W3C Web Performance APIs in Practice

1. Firstly, download [repo](https://github.com/AloisReitbauer/w3cinpractice) via `git clone https://github.com/AloisReitbauer/w3cinpractice`

2. `node server.js` and [Overview](http://localhost:3000/overview.html)

<!--
  which is exactly the same as viewing from the Network [panel](http://en.wikipedia.org/wiki/Panel_(computer_software) -->

--

###  More APIs

1. [Navigation Timing | MDN](https://developer.mozilla.org/en-US/docs/Navigation_timing)
2. [User Timing API: Understanding your Web App - HTML5 Rocks](http://www.html5rocks.com/en/tutorials/webperformance/usertiming/)
3. [10 HTML5 APIs Worth Looking Into](http://www.sitepoint.com/10-html5-apis-worth-looking/)

![Timing life cycle](https://w3c.github.io/resource-timing/resource-timing-overview-1.png)

--

### 3 take aways

1. Browsers dont do any black magics, understand how browsers profile. See [w3 specs](http://w3.org/TR/resource-timing/).

2. Take advantage of caching, including CDN, localstorage.

  1. 170page Book: [High Performance Web Sites](http://shop.oreilly.com/product/9780596529307.do)

  2. [Caching Tutorial](https://www.mnot.net/cache_docs/)

  3. [Google Leverage Browser Caching](https://developers.google.com/speed/docs/insights/LeverageBrowserCaching)

3. Be mindful about performance gain.

--

# Afternoon Section

## 1. Roll Your Own Responsive Design
## -- Jen Kramer
## 2. Transform into a Web Security Guru
## -- Stephen Teilhet

--

### Roll Your Own Responsive Design

1. Let's get responsive, and start asking questions.

2. [Download](http://github.com/jen4web/fluent2015) via `git clone http://github.com/jen4web/fluent2015`

--

<!-- 1  What How  when Why
     2  Why  when How  What -->

## **Questions**

1. What is *responsive* design?

2. Why do we even care responsiveness?

3. How do we achieve/implement it?

--

## **Responses - 1. What is responsive? **

1. According to [Jen](http://twitter.com/jen4web), responsive design can be defined by three characterizes:

  1. Flexible grid based layout

  2. Images that resize

  3. Media quires (CSS)

--

## **Responses - 2. Why do we care? **

1. Provide the **consistent** user experience throughout the product.

2. Allow Users/Customers using **minimal effort** to adopt transition for
different platforms. i.e. iPad, iPhone and Desktop
<!-- Making things smooth -->

3. [Things to consider](http://johnpolacek.github.io/scrolldeck.js/decks/responsive/), *recommend to read*

  1. Time & Money
  2. Older Browsers
  3. Performance
  4. Content, and more

--

## ** Responses - 3. How can we be responsive?**

Responsive examples

1. [The Boston Globe](http://www.bostonglobe.com/)

2. [Target Corp](corporate.target.com)

Counter Example, Airlines, Why?

1. [Southwest](https://www.southwest.com/)

2. [AA](https://www.aa.com)

#### Demo

--

### 3 take aways

1. Know your audiance, [mobile first](http://en.wikipedia.org/wiki/Responsive_web_design)
<!-- Know your audiance's platform, i.e. airlines vs enterprises -->

2. CSS is powerful, dont use JavaScript unless you have to.
<!-- use it and be good at it. -->

3. Fast Internet, does not guarantee fast response.
<!-- People dont have patient, at least not for you -->

--

Tips:

1. Using fonts instead of images

2. [Responsive CSS -- Google](https://developers.google.com/web/fundamentals/layouts/rwd-fundamentals/):

  1. Using viewport, `em` instead of `px`

  2. Using CSS media queries

  3. Using [CSS sprite](https://css-tricks.com/css-sprites/)

  4. know how to choose break points, i.e. screen sizes

3. HiSrc, to support retina display

--

### Transform into a Web Security Guru

1. High level concepts

2. [Info Repo](https://github.com/steilhet/FluentTalkSecurityInfo)

--

## Understand workflow

#### Triangle

Understand the life cycle

```
            /\\
 Security  // \\  Pen-Testing
    SAST  //   \\     DAST
         //     \\
        //_______\\
          AppSec
         Knowledge
```

--

## Understand workflow
#### Overview

Dont reinvent the wheels, see what threats/bugs/vulns already exist.

```
SANS Top 25     OWASP Top 10
       \       /
        v     v
       CWE(vulns)
       /        \
      v          v
   CAPEC         CVE
(attacks)      (observed vulns)
```

--

## Apporaching problems


#### Static Analysis

Source -> Sink(execution), analysis the source code, try to find a hole.

#### Dynamic Analysis

Using a proxy, i.e. OWASP ZAP, sort like brute force.


1 + 1 > 2, combine both tools to dive deep

--

## Tools for automation.

Stand on the shoulders of giants.

1. [Toolswatch](http://www.toolswatch.org)

2. [BEEF](https://github.com/beefproject/beef) exploitation scripting tool

--

## 3 take aways

1. Dont do test on production

2. Keep skills update and look out for current events. i.e. heartbleed and shellshock 2014

3. Be open-mind

--

## FluentConf 2015

#### Summary

**I**nteresting, **I**nsightful, **I**nspiring.

<!--

1.
 Interest topics, FluentConf has various of topics available
 For instance like Go, who would know there would be a topic about go on a
 FrontEnd conference. Web Security, is very intersting,
 I never worked anything like that.

2.
  Insightful knowledges, all the speakers are been around for a while
  web perf, Alois Reitbauer, is in w3 committee.

3.
  Inspiring, CSS, I didnt know CSS can be so powerful to work with browsers
  it gives me hands on experience to work on -->

--

# Thank you
