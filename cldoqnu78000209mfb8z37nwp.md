# How To Create Customizable And Responsive UI Components Using Tailwind

Many companies and individuals, including startups and solopreneurs, use UI components to create the front end of their websites and apps. These components help them communicate their ideas, convert potential customers into actual ones, and connect with their audience. The UI components must be customizable, responsive, and visually captivating.

Most developers, chiefly front-end and full-stack developers, often struggle to build such UI components. This results in the creation of inflexible and unresponsive UI components.

In this article, you will learn how to create customizable and responsive UI components which are flexible, adaptable, and visually appealing using Tailwind CSS.

> "Tailwind CSS is a utility-first CSS framework packed with classes like `flex`, `pt-4`, `text-center` and `rotate-90` that can be composed to build any design directly in your markup." ([Source: Tailwind](https://tailwindcss.com))

## Pre-requisites

To follow along in this article, you need to know of:

* Basic HTML
    
* Basic CSS
    
* Media Queries
    

Let's get started!

## What are Tailwind Components?

Tailwind Components are UI Templates and Components or widgets built using utility classes provided by the Tailwind CSS framework. These classes enable developers to smoothly and rapidly create unique UI elements that are highly customizable.

You can create the components in your preferred Text Editor, such as VS Code, Sublime Text, Atom, or in the Tailwind playground.

Examples of Tailwind components include

* Profile cards
    
* Site headers and footers
    
* Pricing pages
    
* Hero sections
    
* Buttons
    
* Pricing tables
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675331459668/af1db424-aa19-464c-9aec-24685417d1d3.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675331505194/47bb33e5-9ea7-423a-af45-4d0466691690.png align="center")

When you use Tailwind CSS classes to create customizable, reusable, and responsive UI elements, they qualify as Tailwind components.

## Creating your first Tailwind Component

In this tutorial, we shall create a simple, customizable, and responsive site header. For this example, we will use Tailwind's Online Playground, *Tailwind Play.*

> "Tailwind Play is an advanced online playground for Tailwind CSS that lets you use all of Tailwind’s build-time features directly in the browser." (Source: [Tailwind blog](https://tailwindcss.com/blog/introducing-tailwind-play))

It has coding and preview area sections. You can also choose which Tailwind version you want to use while coding.

You will familiarize yourself with the Tailwind Playground as we build the component. If you haven't tried Tailwind yet, you will get a first-hand look at how Tailwind CSS works without any prior installations in your projects.

We shall use icons from [Hero icons](https://heroicons.com/) created by the makers of Tailwind CSS.

### **Getting started with the playground**

**Follow the 3 steps below to get started with the Playground**

**Step-1:**

Go to your browser and visit *https://play.tailwindcss.com*

*The image below shows how the playground looks like*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673945984323/a75a0f1b-9b91-4c29-8a30-02c6c6aeccce.png align="center")

**Second-2:**

Highlight and delete the code in the editor

**Step-3:**

We can now write our code. Let's get started with our component

**We aim for our component to look like this once it's done** ↓

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675025254151/1eb56189-76ad-4ed8-a870-9e91089b024f.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675150302610/9a50af0a-8f1d-48c1-b12e-feacbd4eaa4a.gif align="center")

### **Creating the component**

**A simple responsive site header**

Enter the markup of the component in your editor

```xml
<div class="flex h-screen items-center">
  <header class="flex h-24 w-full items-center justify-around bg-sky-500">
    <div class="logo">
      <h1 class="cursor-pointer text-3xl font-semibold text-gray-100">Tweetos</h1>
    </div>
    <nav class="w-1/2">
      <div class="flex items-center justify-evenly">
        <a href="#">Home</a>
        <a href="#">Pricing</a>
        <a href="#" class="active">Docs</a>
        <a href="#">About</a>
      </div>
    </nav>
    <div>
      <button class="rounded-full bg-blue-600 px-4 py-2 text-white font-semibold">Demo</button>
    </div>
  </header>
</div>
```

Below is how the component looks and behaves after you enter the above markup in the editor.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675146161690/59a243e3-781f-4318-9cb9-61f493988771.gif align="center")

Our site header is progressing nicely! Let's add some active and hover classes to the pages to make them more interactive.

Go to the CSS tab and add these classes for the anchor tags and active class.

```css
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer components {
  .active {
    @apply px-3 py-2 rounded-full bg-white hover:bg-none;
  }
  a {
    @apply [&:not(.active)]:hover:bg-blue-500 px-3 py-2 rounded-full [&:not(.active)]:hover:text-white;
  }
}
```

*A preview of what the above code does*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675145257085/54941682-5781-494f-b4f8-9c4263a8ee03.gif align="center")

Alright, so far so good! The next step is to make the component both responsive, and customizable.

## How To Make Your Component Customizable And Responsive

To make your component customizable and responsive, you need to understand what these terms mean.

Let's find out.

### **Making Your Component Customizable**

To make your component customizable, you need to build it in a way that allows developers or companies to modify and tailor it to their specific needs and preferences.

Creating it in a customizable manner needs you to define its global or theme settings. We shall use the font and color settings for this tutorial. These are the defaults to change to fit a specific theme or brand settings.

**Follow the steps below to define the theme settings of your component**

**Step-1:**

Head to the Config tab. There you will see where to set up your theme settings.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675151661625/0f26fda1-718a-4dcf-8877-33b016f2ef0b.png align="center")

**Step-2**:

Set up the theme settings for your component. In this case, color and font defaults.

```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  theme: {
    extend: {
      colors: {
        'header-background': '#0ea5e9',
        'cta-button-background': '#2563eb',
        'hover-light-blue': '#3b82f6',
        'theme-white': '#ffffff',
        'theme-black': '#000000',
      }
    },
     fontFamily: {
      'headings': ['Open Sans'],
      'plain-text': ['Oswald', 'sans']
    }
  },
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675439594735/bda52b5f-dc88-4e0a-8fd3-4b12d4598c51.png align="center")

> **Note**:
> 
> When you set up your custom colors inside the extend object, you are able to use both them and Tailwind's provided colors. Otherwise, you can only work with the colors you have set up.

Now, change your colors and fonts in the markup and replace them with what you set in your Config file.

*Tailwind colors to replace*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675193074490/a309f9f8-df10-4585-a553-89fc69252d82.png align="center")

*Replacing Tailwind colors with our defined theme colors*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675196375630/2998f027-95fe-4d90-a63f-dab5ceabfcbf.png align="center")

Time to change the fonts, too. Tailwind provides three font families by default and these are sans-serif, serif, and monospaced.

Now time to work on the fonts. Change the fonts of the logo, and pages by using the font class to add our defined fonts in theme settings.

> **Note:** We shall with Tailwind's default fonts for the rest of the tutorial.

You can now change a font or color in your theme settings, and the effect will apply throughout the component without editing every instance in the markup.

Hooray! You have made your component customizable for anyone who wishes to use it. You can do further customizations than this, like spacing and border-radius.

### Making Your Component Responsive

To make your component responsive means that it adapts and looks good on different screen sizes of various devices such as phones, tablets, laptops, and larger monitors.

For this example, we are going to make our component responsive based on the familiar device breakpoints below:

* **Mobile devices**: 320px — 480px.
    
* **iPads and Tablets**: 481px — 768px.
    
* **Small screens and laptops**: 769px — 1024px.
    
* **Desktops and large screens**: 1025px — 1200px.
    
* **Extra large screens**: 1201px, and more.
    

Let's go ahead and add the above breakpoints to our theme settings.

```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  theme: {
    screens: {
      'sm': { min: '320px', max: '480px' },
      'md': { min: '481px', max: '768px' },
      'lg': { min: '769px', max: '1024px' },
      'xl': { min: '1025px', max: '1200px' },
      '2xl': { min: '1201px' },
    },
    extend: {
      colors: {
        'header-background': '#0ea5e9',
        'cta-button-background': '#2563eb',
        'hover-light-blue': '#3b82f6',
        'theme-white': '#ffffff',
        'theme-black': '#000000',
      }
    },
     fontFamily: {
      'headings': ['Open Sans'],
      'plain-text': ['Oswald', 'sans']
    }
  },
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675441105090/b8ae75c5-0ae1-4057-9cb2-31cccc151dd6.png align="center")

We now need to make our component responsive based on the breakpoints in our theme settings.

```xml
<div class="flex h-screen items-center">
  <header class="flex h-24 w-full items-center justify-around bg-header-background">
    <div class="logo">
      <h1 class="sm:text-2xl cursor-pointer text-3xl font-semibold text-theme-white">Tweetos</h1>
    </div>
    <nav class="sm:hidden w-1/2">
      <div class="flex items-center justify-evenly">
        <a href="#">Home</a>
        <a href="#">Pricing</a>
        <a href="#" class="active">Docs</a>
        <a href="#">About</a>
      </div>
    </nav>
    <div>
      <button class="rounded-full bg-cta-button-background px-4 py-2 font-semibold text-theme-white">Demo</button>
    </div>
  </header>
</div>
```

Test the component's responsiveness.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675329026070/690774aa-2b14-4bbf-9243-df03f78e5d30.gif align="center")

Make the component look awesome by using a hamburger menu for smaller screen sizes, as the menu for larger screens won't work.

Let's add a hamburger menu to our HTML markup. Follow the steps below to get going:

1. Visit [Hero icons](https://heroicons.com/)
    
2. Search for a bars-3 menu icon
    
3. Copy the SVG code
    
4. Paste the SVG between the nav tag and the cta-button div
    

After that, add the following classes to the SVG

```xml
<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2.5" stroke="currentColor" class="sm:flex hidden h-8 w-8 cursor-pointer">
      <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
   </svg>
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675330344333/15792c45-9d82-4e23-8a64-c0d0b00f4016.png align="center")

Test the component's responsiveness again

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675150302610/9a50af0a-8f1d-48c1-b12e-feacbd4eaa4a.gif align="left")

Kudos! on making your component both customizable and responsive. One thing is remaining now, testing the responsiveness of the UI element on different devices with varying screen sizes to ensure its responsiveness.

Let's see how we can do responsive testing for the component.

## How To Test The Responsiveness Of Your Component

After you create your Tailwind component, you need to test its responsiveness on different screen sizes. Below are some of the tools you can use for the job.

**Tools:**

* Tailwind Playground
    
* LambdaTest
    
* Chrome dev tools
    

Let's see how you can use each of them.

### **Responsive Testing In Tailwind Playground**

You can test the responsiveness of your component first in the Playground where you created it. It provides a feature for checking the responsiveness of UI elements or components created within it.

To get started, follow the steps below:

* Click the icon in the upper right corner, which is on the left of the light/dark mode icon.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675197191849/ff5ec31e-2efb-4389-b045-f1346dda12ec.png align="center")

* Drag your component's window and see how it responds to different screen sizes defined as defined in your config file.
    
* You can now see its responsiveness in the playground as you adjust the screen size.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675198048133/54a61172-05c0-47e3-a69d-8f4a82bd5570.gif align="center")

You have successfully tested your component's responsiveness using the playground.

You can modify your UI element for better reaction to the screen sizes as you see fit.

### **Responsive Testing Your Component Using Lambdatest**

LambdaTest is an online cross-browser testing tool where you can perform manual and automated tests on multiple devices, browsers, and operating systems.

We are going to use its responsive testing LT Browser 2.0. The LT Browser is a

> "next-gen browser to build, test & debug mobile websites." (Source: [LambdaTest](https://www.lambdatest.com/lt-browser-beta))

To do this, head over to [LamdaTest](https://www.lambdatest.com/lt-browser-beta). After that, follow the below steps to get started with the testing:

* Install the LT Browser on your machine
    
* Launch the browser
    
* Enter the URL of your Tailwind Component in the address bar
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675263153141/30b95e1f-6b23-47b5-91dd-326e65999602.png align="center")
    
    Start testing on any of the available devices
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675263920829/575e89d5-c6d0-4f72-99a0-a7860e726a3c.png align="center")
    
    Do testing on different tablet devices
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675263672776/2e298ae9-b8a5-4309-8bef-5000100b2454.png align="center")
    
    Do testing on various desktop devices
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675263520692/d583809a-9570-46b7-95a6-73b58a873584.png align="center")
    
* Choose a device of your choice on which you wish to test your component, or add a custom one.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675326098857/ac3eca43-7694-458c-808a-97063a1184d2.png align="center")
    

The LT Browser avails you with a couple of features. You can also generate a performance report.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675326204473/ddac6ba3-0526-432f-811f-8c5aa9fc7168.png align="center")

### **Responsive Testing Your Component Using Chrome Dev Tools**

To check your component's responsiveness on different screen sizes and various devices using Chrome Dev tools, follow the below-mentioned steps.

* Right-click on the page, and click inspect.
    
* Click on Preview on the component window
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675358243619/25a8cd4d-f772-4566-bd0e-4b8de03e0078.png align="center")
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675358426671/15278a00-1910-4c8a-8bcc-71cedb94e1ed.png align="center")
    
* Click the *drop-down arrow* at the top of your window.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675245318514/3caf17db-9466-49bb-88a5-b595e560d9c0.png align="center")
    
    Here you can either choose *Responsive* or choose a *device* that you may wish to test your component's responsiveness on.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675243597616/c48cf907-e8cb-4b4a-8b17-dd487c1eda1c.png align="center")
    

**Responsive option**

When you choose the *responsive* option, you will be able to view the response of your component to different screen sizes by resizing the window.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675242205988/51018e78-c44a-42a3-920b-887e3b501ae3.png align="center")

**Devices** **option**

You can decide to test your component's responsiveness on any of the available devices.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675243172921/70216e5e-457b-4057-b86d-79370f8adf7c.png align="center")

If you choose Galaxy Tab S4, for example, your component will look as shown in the image below on that device.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675243719729/63c6fcb7-7abe-4306-93e2-93bcabffd8da.png align="center")

If there is a particular device on which you wish to test your component's responsiveness and it isn't available, you can add it there.

**Follow the below steps to add your custom device**

* Click on the drop-down arrow for devices
    
* Choose the last option of *Edit*
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675244852933/6dbac3da-c9dd-4b5a-932a-c89a29dcde6c.png align="center")
    
* Click on *Add Custom Device.* Enter the device name and dimensions.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675246756763/c59d23b0-e5d0-46df-9bd8-98720158e11d.png align="center")
    
* You can now start responsive testing your component on the custom device you have just added to the Dev Tools.
    

Tests help you know how your component responds to different devices of various screen sizes, so you can easily decide how to resolve any issues found.

Here is the link to the component we have just created: [Visit component.](https://play.tailwindcss.com/ns3VjWOvHA)

Feel free to tweak things up 😉

## How To Get Component Ideas

**Get ideas from design inspiration websites**

Visit UI inspiration websites such as Dribble, Behance, and Awwwards to get component ideas to create.

UI/UX designers provide the public with free UI designs for use and inspiration through these websites. Some of the designs include landing pages, login forms, signup forms, and pricing tables.

## Giving You Inspiration

Below are some Tailwind Components I have created. Feel free to check them out, play with them, and add or remove something. Have fun 😊

I share them with you in the hopes that they inspire you to create your first Tailwind Component.

Take a look, take inspiration. ↓

* **Pricing Table**
    
    Visit [`Pricing table`](https://play.tailwindcss.com/MotbiAE6Ja)
    

![Responsive Pricing Table made using Tailwind CSS](https://cdn.hashnode.com/res/hashnode/image/upload/v1673790129325/487f82da-e263-4ec4-8fd3-792718d097c8.png align="right")

* Pricing page
    
    Visit [`Pricing page`](https://play.tailwindcss.com/r5tIZ6enXE)
    
    ![Responsive Pricing page made in Tailwind CSS](https://cdn.hashnode.com/res/hashnode/image/upload/v1673949415038/26765ec5-b60e-4104-9b72-6538103df280.png align="center")
    

If you find the components fascinating and would like to explore more for your learning and practice, check out this [GitHub Repository](https://github.com/MbaziiraRonald/Tailwind_Components) that contains additional components I created. Use them to learn and practice while creating widgets or putting your Tailwind knowledge to practice. 

## Conclusion

You have learned how to create customizable and responsive UI components using Tailwind CSS. Now, I suggest you go try out creating your first Tailwind component. I promise you are going to enjoy it.

Happy coding. Happy learning!

%%[buy-me-a-coffee]