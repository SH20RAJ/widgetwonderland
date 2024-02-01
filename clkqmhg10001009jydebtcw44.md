---
title: "Create Your Own URL Shortener on Blogger"
seoTitle: "Title: Create Your Own URL Shortener for Blogger with Widget Wonderlan"
seoDescription: "Introduction: Welcome to Widget Wonderland, where we embark on a magical journey through the world of Blogger widgets! At Widget Wonderland, we are passiona"
datePublished: Mon Jul 31 2023 08:42:58 GMT+0000 (Coordinated Universal Time)
cuid: clkqmhg10001009jydebtcw44
slug: create-your-own-url-shortener-on-blogger

---

Title: Create Your Own URL Shortener for Blogger with Widget Wonderland's Magical Widget Codes

Introduction: Welcome to Widget Wonderland, where we embark on a magical journey through the world of Blogger widgets! At Widget Wonderland, we are passionate about helping bloggers enhance their websites with creative and useful widget codes. In this tutorial, we will guide you through the process of creating your very own URL shortener for Blogger using Rebrandly API, LocalStorage, Bootstrap, and jQuery. Don't worry; we've got you covered with our handpicked collection of widget codes! Before we begin, please ensure you have switched to the first-generation Blogger theme to proceed. Let's dive in and unlock the potential of your blog with our whimsical URL shortener!

**Step 1: Getting Started**

1. First, make sure you have switched to the first-generation Blogger theme. Go to your Blogger dashboard, navigate to "Theme" in the left sidebar, and select "Revert to classic theme."
    
2. Next, turn off the Blogger navbar to create a clean and seamless experience for your readers. To do this, go to "Layout" in the left sidebar, click on "Navbar," and then select "Off."
    

**Step 2: Prepare the URL Shortener Code** Now, let's prepare the URL shortener code by adjusting it for your Blogger site.

1. Replace `'YOUR_REBRANDLY_API_KEY'` with your actual Rebrandly API key in the script section. If you haven't registered with Rebrandly, sign up for an account at [https://www.rebrandly.com/](https://www.rebrandly.com/) and obtain your API key.
    
2. Remove the `<!DOCTYPE html>` and `<html>` tags from the code since Blogger handles the overall page structure.
    
3. Delete the `<head>` section with the Bootstrap CSS and other scripts, as Blogger will manage the inclusion of CSS and JavaScript.
    
4. Modify the `<footer>` section to match the footer of your Blogger theme. Add a backlink to our blog "Widget Wonderland" ([https://widgetwonderland.hashnode.dev/](https://widgetwonderland.hashnode.dev/)) with the anchor text "Widget Wonderland."
    

Here's the updated URL shortener code for your Blogger site:

```html
<!-- Paste the full code here -->
<div class="container mt-5">
  <h1>URLy - Link Shortener</h1>
  <form id="shortenForm" class="mt-3">
    <div class="input-group">
      <input type="text" id="urlInput" class="form-control" placeholder="Enter your URL here" required>
      <div class="input-group-append">
        <button type="submit" class="btn btn-primary">Shorten URL</button>
      </div>
    </div>
  </form>
  <div id="shortenedURLContainer" class="mt-3" style="display: none;">
    <h2>Shortened URL:</h2>
    <div class="input-group">
      <input type="text" id="shortenedURL" class="form-control" readonly>
      <div class="input-group-append">
        <button id="copyButton" class="btn btn-secondary">Copy</button>
      </div>
    </div>
  </div>
  <div class="mt-5">
    <h2>Saved Shortened URLs:</h2>
    <table class="table table-bordered">
      <thead>
        <tr>
          <th>Shortened URL</th>
          <th>Full URL</th>
          <th>Date Time</th>
          <th>Copy</th>
        </tr>
      </thead>
      <tbody id="savedLinksBody">
      </tbody>
    </table>
  </div>
</div>

<footer class="text-center mt-5">
  <p>&copy; 2023 URLy - Link Shortener. All rights reserved. | <a href="https://widgetwonderland.hashnode.dev/">Widget Wonderland</a></p>
</footer>

<script>
  // ... (Complete script code from the previous steps) ...
</script>
```

**Step 3: Integrate the URL Shortener on Blogger** To integrate the URL shortener into your Blogger posts or pages:

1. In your Blogger dashboard, create a new post or edit an existing one where you want to add the URL shortener.
    
2. Switch to the HTML editor mode by clicking on the "HTML" button in the post editor.
    
3. Paste the prepared URL shortener code into the HTML editor.
    
4. Switch back to the "Compose" mode to see a preview of the URL shortener.
    
5. Save or publish the post to make the URL shortener live on your Blogger site.
    

**Step 4: Verify the Functionality** To verify that the URL shortener is working correctly, access the post where you embedded the code and enter a long URL in the input field. Click on the "Shorten URL" button, and the shortened URL will be displayed below. Additionally, the shortened URL will be saved in the "Saved Shortened URLs" table.

Here is the Full Code to Copy

```xml
<!DOCTYPE html>
<html>
<head>
  <title>URLy - Link Shortener</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Bootstrap CSS -->
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
</head>
<body>
  <div class="container mt-5">
    <h1>URLy - Link Shortener</h1>
    <form id="shortenForm" class="mt-3">
      <div class="input-group">
        <input type="text" id="urlInput" class="form-control" placeholder="Enter your URL here" required>
        <div class="input-group-append">
          <button type="submit" class="btn btn-primary">Shorten URL</button>
        </div>
      </div>
    </form>
    <div id="shortenedURLContainer" class="mt-3" style="display: none;">
      <h2>Shortened URL:</h2>
      <div class="input-group">
        <input type="text" id="shortenedURL" class="form-control" readonly>
        <div class="input-group-append">
          <button id="copyButton" class="btn btn-secondary">Copy</button>
        </div>
      </div>
    </div>
    <div class="mt-5">
      <h2>Saved Shortened URLs:</h2>
      <table class="table table-bordered">
        <thead>
          <tr>
            <th>Shortened URL</th>
            <th>Full URL</th>
            <th>Date Time</th>
            <th>Copy</th>
          </tr>
        </thead>
        <tbody id="savedLinksBody">
        </tbody>
      </table>
    </div>
  </div>

  <footer class="text-center mt-5">
    <p>&copy; 2023 URLy - Link Shortener. All rights reserved. <a href="https://codexdindia.blogspot.com/tools" rel="dofollow" target="_blank">CXDIIN</a></p>
  </footer>

  <!-- Bootstrap JS and jQuery -->
  <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.1/dist/umd/popper.min.js"></script>
  <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>

  <script>
    const API_KEY = '2259516283a549eea99744549057302f';
    const API_URL = 'https://api.rebrandly.com/v1/links';

       // Check if local storage is available in the browser
    const isLocalStorageSupported = typeof Storage !== 'undefined';

    // Function to display saved links from local storage
    function displaySavedLinks() {
      const savedLinks = JSON.parse(localStorage.getItem('shortenedLinks')) || [];
      const savedLinksBody = document.getElementById('savedLinksBody');
      savedLinksBody.innerHTML = '';

      savedLinks.forEach((linkInfo) => {
        if (true) {
          const newRow = document.createElement('tr');

          const shortUrlCell = document.createElement('td');
          const fullUrlCell = document.createElement('td');
          const dateTimeCell = document.createElement('td');
          const copyCell = document.createElement('td');

          const shortUrlNode = document.createTextNode(linkInfo.shortUrl);
          const fullUrlNode = document.createTextNode(linkInfo.fullUrl);
          const dateTimeNode = document.createTextNode(linkInfo.dateTime);

          const copyButton = document.createElement('button');
          copyButton.className = 'btn btn-secondary';
          copyButton.textContent = 'Copy';
          copyButton.addEventListener('click', () => {
            copyToClipboard(linkInfo.shortUrl);
          });
          console.log(shortUrlNode);
          shortUrlCell.appendChild(shortUrlNode);
          fullUrlCell.appendChild(fullUrlNode);
          dateTimeCell.appendChild(dateTimeNode);
          copyCell.appendChild(copyButton);

          newRow.appendChild(shortUrlCell);
          newRow.appendChild(fullUrlCell);
          newRow.appendChild(dateTimeCell);
          newRow.appendChild(copyCell);

          savedLinksBody.appendChild(newRow);
        }
      });
    }

    // Display saved links on page load
    window.addEventListener('load', () => {
      displaySavedLinks();
    });


    document.getElementById('shortenForm').addEventListener('submit', (event) => {
      event.preventDefault();

      const inputElement = document.getElementById('urlInput');
      const urlToShorten = inputElement.value;

      shortenURL(urlToShorten)
        .then((shortenedURL) => {
          const shortenedURLContainer = document.getElementById('shortenedURLContainer');
          const shortenedURLElement = document.getElementById('shortenedURL');
          const copyButton = document.getElementById('copyButton');

          shortenedURLElement.value = shortenedURL.shortUrl;
          shortenedURLContainer.style.display = 'block';

          if (isLocalStorageSupported) {
            // Save the shortened link info in local storage
            const savedLinks = JSON.parse(localStorage.getItem('shortenedLinks')) || [];
            savedLinks.push({
              shortUrl: shortenedURL.shortUrl,
              fullUrl: urlToShorten,
              dateTime: new Date().toLocaleString(),
            });
            localStorage.setItem('shortenedLinks', JSON.stringify(savedLinks));

            // Display updated saved links
            displaySavedLinks();
          }

          // Enable the copy button
          copyButton.disabled = false;
        })
        .catch((error) => {
          console.error('Error shortening URL:', error);
        });
    });

    function copyToClipboard(text) {
      const tempElement = document.createElement('textarea');
      tempElement.value = text;
      document.body.appendChild(tempElement);
      tempElement.select();
      document.execCommand('copy');
      document.body.removeChild(tempElement);
      alert('Copied to clipboard!');
    }

    async function shortenURL(url) {
      const response = await fetch(API_URL, {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
          'apikey': API_KEY,
        },
        body: JSON.stringify({
          destination: url,
        }),
      });

      if (!response.ok) {
        throw new Error('Failed to shorten URL');
      }

      return response.json();
    }
  </script>
</body>
</html>
```

Conclusion: Congratulations on integrating your own URL shortener on your Blogger website with the help of our Widget Wonderland's magical widget codes! Your blog is now equipped with a whimsical URL shortener that will make sharing links easier and more enjoyable for your readers. Remember to switch to the first-generation Blogger theme and turn off the navbar to create a seamless experience. Keep exploring Widget Wonderland for more enchanting widget codes to enhance your blog. Happy blogging!