---
title: "Random Quotes Widget - Blogger"
seoTitle: "Unleash Wisdom with a Random Quotes Widget: A Guide."
seoDescription: "Quotes have a magical ability to inspire, motivate, and touch the hearts of readers. As a blogger, you can weave this magic into your blog with a Quote."
datePublished: Thu Jul 27 2023 04:07:19 GMT+0000 (Coordinated Universal Time)
cuid: clkkmvjxg000509juhx71264y
slug: random-quotes-widget-blogger

---

**Title: Unleash Wisdom with a Random Quotes Widget: A Guide to Captivate Your Readers**

*Introduction*

Quotes have a magical ability to inspire, motivate, and touch the hearts of readers. As a blogger, you can weave this magic into your blog with a Random Quotes Widget. In this guide, we'll embark on a journey to create a captivating Random Quotes Widget that will enchant your readers with nuggets of wisdom and inspiration. Let's dive into the creation process and mesmerize your audience with the power of words!

*The Power of a Random Quotes Widget*

The Random Quotes Widget offers several enchanting benefits for your blog:

1. **Reader Engagement**: Captivate your readers with fresh and meaningful quotes every time they visit your blog.
    
2. **Inspiration and Reflection**: Touch the hearts of your audience with quotes that inspire, motivate, and promote reflection.
    
3. **Enhanced Aesthetics**: Elevate your blog's design with a dynamic widget that adds charm and intrigue.
    
4. **Personal Connection**: Connect with your readers on a deeper level by sharing quotes that resonate with them.
    

*Creating the Random Quotes Widget*

**Step 1: Gathering Quotes**

Begin by gathering a collection of quotes that align with the theme and tone of your blog. You can choose quotes from famous personalities, literature, movies, or even write your own original quotes.

**Step 2: HTML Structure**

Add the following HTML code where you want the Random Quotes Widget to appear:

```html
<div class="random-quotes-widget">
  <blockquote class="quote" id="quote-text">Loading...</blockquote>
  <p class="author" id="quote-author"></p>
  <button class="btn" id="new-quote-btn">New Quote</button>
</div>
```

**Step 3: CSS Enchantment**

Add the following CSS to your blog's stylesheet or within `<style>` tags:

```css
.random-quotes-widget {
  background-color: #f2f2f2;
  border-radius: 10px;
  padding: 20px;
  text-align: center;
}

.quote {
  font-size: 24px;
  font-style: italic;
  margin-bottom: 10px;
}

.author {
  font-size: 16px;
  color: #666;
}

.btn {
  background-color: #4CAF50;
  color: #fff;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn:hover {
  background-color: #45a049;
}
```

**Step 4: JavaScript Magic**

Add the following JavaScript code just before the closing `</body>` tag or within `<script>` tags:

```html
<script>
  const quotes = [
    // Add your quotes here (e.g., { text: "Quote text", author: "Author" })
    // You can add as many quotes as you like
  ];

  const quoteElement = document.getElementById('quote-text');
  const authorElement = document.getElementById('quote-author');
  const newQuoteButton = document.getElementById('new-quote-btn');

  function getRandomQuote() {
    const randomIndex = Math.floor(Math.random() * quotes.length);
    return quotes[randomIndex];
  }

  function displayRandomQuote() {
    const randomQuote = getRandomQuote();
    quoteElement.textContent = randomQuote.text;
    authorElement.textContent = `- ${randomQuote.author}`;
  }

  newQuoteButton.addEventListener('click', displayRandomQuote);

  // Display a random quote when the page loads
  displayRandomQuote();
</script>
```

**Step 5: Displaying the Widget**

Now, your Random Quotes Widget is ready to enchant your blog with refreshing and inspiring quotes. Customize the `quotes` array by adding your collection of quotes with their respective authors.

*Conclusion*

Congratulations! You've successfully woven a Random Quotes Widget that will enchant your blog with fresh inspiration and wisdom every time it's visited. With the power of captivating CSS and JavaScript magic, your readers will be spellbound by the dynamic display of thought-provoking quotes.

As you embrace the enchantment of this Random Quotes Widget, you'll foster deeper connections with your readers and create an inspiring atmosphere on your blog. Happy blogging, and may your widget cast a spell of wonder and reflection on your readers!

# Using API

To create a Random Quotes Widget using an external Quotes API, we'll use the [Forismatic API](http://forismatic.com/en/api/) that provides a wide range of quotes. Follow the steps below to create the widget:

**Step 1: Access the Forismatic API**

The Forismatic API does not require an API key. We can directly access the API to fetch random quotes. The API endpoint for random quotes is:

```plaintext
http://api.forismatic.com/api/1.0/?method=getQuote&format=json&lang=en
```

**Step 2: HTML Structure**

Add the following HTML code where you want the Random Quotes Widget to appear:

```html
<div class="random-quotes-widget">
  <blockquote class="quote" id="quote-text">Loading...</blockquote>
  <p class="author" id="quote-author"></p>
  <button class="btn" id="new-quote-btn">New Quote</button>
</div>
```

**Step 3: CSS Enchantment**

Add the following CSS to your blog's stylesheet or within `<style>` tags:

```css
.random-quotes-widget {
  background-color: #f2f2f2;
  border-radius: 10px;
  padding: 20px;
  text-align: center;
}

.quote {
  font-size: 24px;
  font-style: italic;
  margin-bottom: 10px;
}

.author {
  font-size: 16px;
  color: #666;
}

.btn {
  background-color: #4CAF50;
  color: #fff;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn:hover {
  background-color: #45a049;
}
```

**Step 4: JavaScript Magic**

Add the following JavaScript code just before the closing `</body>` tag or within `<script>` tags:

```html
<script>
  const quoteElement = document.getElementById('quote-text');
  const authorElement = document.getElementById('quote-author');
  const newQuoteButton = document.getElementById('new-quote-btn');

  function getQuote() {
    fetch('http://api.forismatic.com/api/1.0/?method=getQuote&format=json&lang=en')
      .then(response => response.json())
      .then(data => {
        quoteElement.textContent = data.quoteText;
        authorElement.textContent = `- ${data.quoteAuthor || 'Unknown'}`;
      })
      .catch(error => {
        console.error('Error fetching quote:', error);
      });
  }

  newQuoteButton.addEventListener('click', getQuote);

  // Display a random quote when the page loads
  getQuote();
</script>
```

**Step 5: Displaying the Widget**

Now, your Random Quotes Widget is ready to enchant your blog with random quotes fetched from the Forismatic API.

*Conclusion*

Congratulations! You've successfully crafted a Random Quotes Widget that fetches quotes dynamically from the Forismatic API. With the power of captivating CSS and JavaScript magic, your readers will be spellbound by the ever-changing display of inspiring quotes.

As you embrace the enchantment of this Random Quotes Widget, the wisdom and inspiration it brings will resonate with your readers, creating an atmosphere of reflection and motivation on your blog. Happy blogging, and may your widget cast a spell of wonder and inspiration on your readers!

As you embrace the enchantment of this Weather Widget, don't forget to attribute the inspiration from [WidgetWonderland](https://widgetwonderland.hashnode.dev/) and [CodexDIndia](https://codexdindia.blogspot.com/), who have paved the way for captivating widgets. Happy blogging, and may your weather widget charm your readers with its spellbinding magic!