# Sprint Challenge: Advanced CSS - Space Walkers Web Page

This challenge allows you to practice the concepts and techniques learned over the past week and apply them in a concrete project. This Sprint explored advanced CSS techniques using Responsive Design and Preprocessing. During this Sprint, you studied how to use the viewport meta tag, media queries, setting up a preprocessor, and advanced use of preprocessing techniques. In your challenge this week, you will demonstrate proficiency by updating a website that is missing content as well as adding mobile styling.

## Instructions

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the Sprint Challenge. However, you are encouraged to follow the twenty-minute rule and seek support from your PM and Instructor in your cohort help channel on Slack. Your work reflects your proficiency in advanced css and your command of the concepts and techniques in responsive web design and preprocessing.

You have three hours to complete this challenge. Plan your time accordingly.

## Commits

Commit your code regularly and meaningfully. This helps both you (in case you ever need to return to old code for any number of reasons) and your project manager.

## Description

The client for this challenge is _Spacewalkers Magazine_. Spacewalkers needs your help to build a small proof of concept website for their marketing team. They have provided designs for both desktop and phone views. In addition to designs and content they have most of the home page coded for you. You just need to finish the navigation and header as well as the mobile styles.

In meeting the minimum viable product (MVP) specifications listed below, your web page should look like the solution design files of the desktop and mobile views:

[Click here to review the home design](design-files/home-desktop.png)

[Click here to review the mobile design](design-files/home-mobile.png)

## Self-Study Questions

Demonstrate your understanding of this week's concepts by answering the following free-form questions.

Edit this document to include your answers after each question. Make sure to leave a blank line above and below your answer so it is clear and easy to read by your project manager

1. What is the difference between an adaptive website and a fully responsive website?

Responsive sites and adaptive sites are the same in that they both change appearance based on the browser environment they are being viewed on (the most common thing: the browser's width).

Responsive websites respond to the size of the browser at any given point. No matter what the browser width may be, the site adjusts its layout (and perhaps functionality) in a way that is optimized to the screen.

Adaptive websites adapt to the width of the browser at a specific points. In other words, the website is only concerned about the browser being a specific width, at which point it adapts the layout.

Another way to think about it is the difference between smooth and snap design. Responsive design is smooth because the layout fluidly adjusts regardless of what device it is viewed on. Adaptive design, on the other hand, snaps into place because the page is serving something different because of the browser or device it is viewed on.

2. Describe what it means to be mobile first vs desktop first.

The mobile-first approach is exactly as it sounds: designing for the smallest screen and working your way up.The mobile-first approach is a tenet of progressive enhancement.

It is the ideology that mobile design, as the hardest, should be done first. Once the mobile design questions are answered, designing for other devices will be easier. What it boils down to is that, the smallest of the designs will have only the essential features, so right away you have designed the heart of your UX.

Desktop first takes the opposite approach, the theory behind desktop first design is graceful degradation. This incorporates all of the complexities right from the start, then strips them away later for smaller devices. The problem with graceful degradation is that when you build the all-inclusive design right from the start, the core and supplementary elements merge and become harder to distinguish and separate. The entire philosophy runs the risk of treating mobile design as more of an afterthought since you’re “cutting down” the experience.


3. What does `font-size: 62.5%` in the `html` tag do for us when using `rem` units?

html { font-size: 62.5%; }
this makes the default font size for your entire website 10px (assuming the browser’s default font size is 16px, which is the standard but is also user-configurable). Thus making conversion rem <-> px (pixels) is very easy (just divide pixel value by 10).

This can serve as a fallback for older browsers that don't support the rem unit such as IE8, Firefox 3.5, Safari 4 and Opera 11.

A typical method is to set the HTML font-size to 62.5%. That's because 62.5% of 16px (typical default browser font-size) is 10px. That would still make 1.6rem = 16px. This now means that if the user's default browser font-size is changed to, for example, 20px, 1.6rem would now equal 20px.


4. How would you describe preprocessing to someone new to CSS?

CSS itself is static in the sense that it doesn't provide for logical blocks, resuable values, or self-contained functions. Preprocessors such as LESS and SASS add such functionality, creating a sort of CSS superset. These are written differently, though they resemble closely CSS. Because browsers expect plain CSS, styles written in one of the preprocessors will need to be processed into CSS.

A CSS preprocessor is a way to add conditional logic and/or writing efficiency to the process of making CSS. Since CSS is relatively verbose and contains no built in conditional logic, this is a way to achieve those things.

It's a pre processor because CSS is static. The browser demands a flat file, so all of that has to happen before the CSS file is published, hence the preprocessor.

5. What is your favorite concept in preprocessing? What is the concept that gives you the most trouble?

Nesting is my favorite concept because it follows the best practice nesting conventions of writing html and helps you (me) stay on track, logically, as opposed to writing CSS styles as the come up. In other words, Nesting creates the visual hierarchy, as in HTML, that CSS innately lacks and thus increases readability.

I think splitting the code into multiple files is giving me the most trouble at this point because it is hard for me to visualize conflicts (side effects) associated with Cascading


You are expected to be able to answer all these questions. Your responses contribute to your Sprint Challenge grade. Skipping this section *will* prevent you from passing this challenge.

## Project Set Up

Follow these steps to set up your project:

### Git Set up

- [ ] Create a forked copy of this project.
- [ ] Add your project manager as collaborator on Github.
- [ ] Clone your OWN version of the repository (Not Lambda's by mistake!).
- [ ] Create a new branch: git checkout -b `<firstName-lastName>`.
- [ ] Implement the project on your newly created `<firstName-lastName>` branch, committing changes regularly.
- [ ] Push commits: git push origin `<firstName-lastName>`.

Follow these steps for completing your project.

- [ ] Submit a Pull-Request to merge <firstName-lastName> Branch into master (student's  Repo). **Please don't merge your own pull request**
- [ ] Add your project manager as a reviewer on the pull-request
- [ ] Your project manager will count the project as complete by merging the branch back into master.


### Preprocessor Set up

* [ ] Verify that you have LESS installed correctly by running `lessc -v` in your terminal, if you don't get a version message back, reach out to your project manager for help.
* [ ] Open your terminal and navigate to your preprocessing project by using the `cd` command
* [ ] Once in your project's root folder, run the following command `less-watch-compiler less css index.less`
* [ ] Verify your compiler is working correctly by changing the `background-color` on the `html` selector to `red` in your `index.less` file.
* [ ] Once you see the red screen, you can delete that style and you're ready to start on the next task

## Minimum Viable Product

Your finished project must include all of the following requirements:

### Import LESS Files

* [ ] Navigate to your `index.less` file. Notice the file is blank. You have been asked to use a certain import order. That order is as follows:

```markdown
1.variables.less
2.mixins.less
3.reset.less
4.global.less
5.navigation.less
6.footer.less
7.home-page.less
```

_You will know everything is working properly when you see the styles enabled for the provided content._  

### Home Page - Desktop HTML & LESS

* [ ] Take 10 minutes to review the code that has already been provided for you. Take time to see how the home page was built.

* [ ] Add a viewport meta tag to the head of your index.html page

* [ ] [Review the provided home desktop design file](design-files/home-desktop.png). You are to build the missing navigation system and header image. You have been provided all content necessary in the [index.html file](index.html)

* [ ] Navigation Styles: Use the `navigation.less` file for styling.

* [ ] Main Content Styles: Use the `home-page.less` file for styling

* [ ] LESS Mixins: Create and use 2 different mixins to aid your styling. Use the `mixins.less` file for your mixins

* [ ] LESS Parametric Mixin: create a parametric mixin that is used to create the `sign up` button styles.

* [ ]  Use at least 2 parameters to create your button

* [ ] Create a hover state that swaps the background color and font color of the base button styles.

### Mobile Design

* [ ] Create a `@phone` variable that contains a `max-width: 500px` media query string. Use the `@phone` variable for all your nested mobile styling.

* [ ] [Review the provided home mobile design file](design-files/home-mobile.png). Match your mobile styling the best you can using the design file.

* [ ] Push your changes and create a pull request if you haven't already.

In your solution, it is essential that you follow best practices and produce clean and professional results. Schedule time to review, refine, and assess your work and perform basic professional polishing including spell-checking and grammar-checking on your work. It is better to submit a challenge that meets MVP than one that attempts too much and does not.

## Stretch Problems

After finishing your required elements, you can push your work further. These goals may or may not be things you have learned in this module but they build on the material you just studied. Time allowing, stretch your limits and see if you can deliver on the following optional goals:

* [ ] Build a page of your choosing from the navigation items. Come up with content and images that fit the theme.

* [ ] Introduce CSS animations to your site.

* [ ] Create a fixed navigation and add some opacity to the background

* [ ] Create a form that would allow someone to sign up for a Spacewalkers Magazine subscription
