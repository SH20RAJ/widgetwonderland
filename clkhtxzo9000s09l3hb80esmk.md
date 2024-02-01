---
title: "Random Posts Widget - Blogger"
seoTitle: "The Magic of Blogger Widgets: Your First Random Posts Widget"
seoDescription: "Discovering the Magic of Blogger Widgets: Your First Random Posts Widget"
datePublished: Tue Jul 25 2023 05:01:52 GMT+0000 (Coordinated Universal Time)
cuid: clkhtxzo9000s09l3hb80esmk
slug: random-posts-widget-blogger
canonical: https://codexdindia.blogspot.com/
tags: random-posts-widget

---

**Title: Unlocking the Magic of Blogger Widgets: Your First Random Posts Widget**

*Introduction*

Welcome to the enchanting world of Blogger widgets, where a single line of code can breathe life into your blog. As a new blogger, you're about to embark on a journey filled with creativity and excitement. In this inaugural post, we'll explore the wonders of a Random Posts Widget, a charming addition that will captivate your readers and keep them coming back for more.

*Unveiling the Random Posts Widget*

The Random Posts Widget is a delightful feature that displays a selection of random posts from your blog. Each time a visitor lands on your blog, they'll be treated to a surprise—a curated assortment of posts they might have missed otherwise. It's a fantastic way to engage your audience and entice them to explore more of your content.

*Step-by-Step Installation*

Fear not, for the magic of Blogger widgets is easily within your grasp. Follow these simple steps to add the Random Posts Widget to your blog:

**Step 1: Access Your Blogger Dashboard**

Log in to your Blogger account and navigate to the Blogger Dashboard.

**Step 2: Access the "Layout" Section**

On the left-hand sidebar, click on "Layout." This is where you can customize the layout of your blog.

**Step 3: Add a Gadget**

Look for the section of your blog layout where you'd like to place the Random Posts Widget (e.g., sidebar or footer). Click on "Add a Gadget" within that section.

**Step 4: Select the HTML/JavaScript Gadget**

In the pop-up window that appears, scroll down and choose the "HTML/JavaScript" gadget.

**Step 5: Copy and Paste the Code**

Now, you'll see a text box where you can enter your custom code. Copy the following code and paste it into the text box:

```html
<div class="custom-random-posts-widget">
  <h2>Random Posts</h2>
  <ul id="random-posts-list"></ul>
</div>

<script>
  function getFiveRandomPosts(data) {
    var posts = data.feed.entry;
    var numPosts = posts.length;
    var randomIndexes = [];
    var limit = 5;

    while (randomIndexes.length < limit) {
      var randomIndex = Math.floor(Math.random() * numPosts);
      if (randomIndexes.indexOf(randomIndex) === -1) {
        randomIndexes.push(randomIndex);
      }
    }

    var randomPosts = [];
    for (var i = 0; i < limit; i++) {
      var post = posts[randomIndexes[i]];
      var postTitle = post.title.$t;
      var postUrl = post.link.filter(link => link.rel === 'alternate')[0].href;

      // Grabbing the poster image (optional, user-configurable)
      var postImageUrl = post.media$thumbnail ? post.media$thumbnail.url : '';
      var posterImage = postImageUrl ? '<img src="' + postImageUrl + '" alt="' + postTitle + '">' : '';

      randomPosts.push('<li>' + posterImage + '<a href="' + postUrl + '">' + postTitle + '</a></li>');
    }

    document.getElementById('random-posts-list').innerHTML = randomPosts.join('');
  }

  function loadScript(url) {
    var script = document.createElement('script');
    script.src = url;
    document.getElementsByTagName('head')[0].appendChild(script);
  }

  loadScript('/feeds/posts/summary?alt=json-in-script&max-results=100&callback=getFiveRandomPosts');
</script>

<style>
  /* Customize the widget's style here */
  .custom-random-posts-widget {
    font-family: Arial, sans-serif;
    background-color: #f1f1f1;
    padding: 15px;
  }

  .custom-random-posts-widget h2 {
    margin-bottom: 10px;
    font-size: 18px;
    font-weight: bold;
  }

  .custom-random-posts-widget ul {
    list-style: none;
    padding: 0;
  }

  .custom-random-posts-widget li {
    margin-bottom: 5px;
  }

  .custom-random-posts-widget a {
    color: #333;
    text-decoration: none;
  }

  .custom-random-posts-widget a:hover {
    text-decoration: underline;
  }
</style>
```

**Step 6: Save and Enjoy!**

Click "Save" to add the Random Posts Widget to your blog. Now, visit your blog's homepage, and you'll witness the magic as the widget displays five random posts each time the page loads!

*Customizing the Widget*

While the provided code is designed to seamlessly blend with your current Blogger theme, you can customize the widget's appearance to match your blog's style. Explore the `<style>` section within the code to change fonts, colors, padding, and more.

*Join the Widget Wonderland!*

For more exciting Blogger widget codes and tips, visit [Widget Wonderland](https://widgetwonderland.hashnode.dev/). Discover the magical possibilities that Blogger widgets offer and turn your blog into a captivating wonderland.

*Discover More Tech Insights*

Explore tech tutorials and coding adventures at [CodexDIndia](https://codexdindia.blogspot.com/). Unleash your inner tech enthusiast and embark on a journey of continuous learning.

*Conclusion*

Congratulations on adding your first Blogger widget—a Random Posts Widget that promises to enchant your readers with each visit. But this is just the beginning of your Widget Wonderland journey. Stay tuned for more captivating widget codes that will elevate your blogging experience to new heights. Embrace the magic of Blogger widgets, and let your creativity shine through! Happy blogging!