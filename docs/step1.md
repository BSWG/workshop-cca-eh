## Step 1: Getting started

Let's replace the default application with something more unique. This involves changing the default HTML, JS and CSS files.

#### HTML

Open `index.html`, and update the `<head>` to look like this:

    <head>
      <title>Eh</title>
      <link rel="stylesheet" href="styles.css">
      <link rel="import" href="ui/vulcanized.html"><!-- generated by prepare.sh -->
      <script src="main.js"></script>
    </head>

And update `<body>` with our default Polymer elements and `eh-contact-list`:

    <body unresolved>
      <core-header-panel>
        <core-toolbar>
          <h3 flex>Eh</h3>
        </core-toolbar>

        <eh-contact-list id="contacts"></eh-contact-list>

      </core-header-panel>
    </body>

#### JS

Now that our app is Polymer-based, we need to listen for the `polymer-ready` event to get started. Replace the contents of `main.js`, our foreground script, with this:

    window.addEventListener('polymer-ready', function(e) {
      var contacts = [
        { name: "Loonie" },
        { name: "Toonie" }
      ];
      document.getElementById('contacts').contacts = contacts;
    });

We'll add more code in here later. But for now, this just creates a couple of test contacts.

#### CSS

Finally, the page needs a coat of paint.  Replace the contents of `styles.css` with this:

    html, body {
      height: 100%;
      margin: 0;
      background-color: #E5E5E5;
    }

    body {
      overflow: auto;
      font-family: "Lucida Grande", Verdana, Helvetica, Arial, Sans-serif;
    }

    core-header-panel {
      height: 100%;
      overflow: auto;
      -webkit-overflow-scrolling: touch;
    }

    core-toolbar {
      background: #03a9f4;
      color: white;
      font-size: 48px;
    }

### Play It Again

If you run your app again, you should see something like this:

![Preview](https://github.com/MobileChromeApps/workshop-cca-eh/raw/master/docs/assets/step1-preview.png)

Congratulations!

### Getting Stuck?

If you ever get stuck, you can find the "answers" inside the `workshop/` folder.  The code for this step is in [step1](https://github.com/MobileChromeApps/workshop-cca-eh/blob/master/workshop/step1).

### How's It Going, Eh?

_**Continue to [Step 2: Google Cloud Messaging &raquo;](https://github.com/MobileChromeApps/workshop-cca-eh/blob/master/docs/step2.md)**_
