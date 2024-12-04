# Website creation

Two points to consider:

1. Create the website (locally)
2. Deploy the website online

## How to create a website ?

A website is built using various client-side languages such as HTML, CSS, and JavaScript.

- **HTML** provides the structure of the website, organizing content like text, images, and other media.
- **CSS** complements HTML by defining the visual style of the website, including elements like colors, fonts, and layouts.
- **JavaScript** adds interactivity to the website, enabling more complex features like dynamic content, form validation, and animations.

Web browsers interpret HTML, CSS, and JavaScript to render websites in a format that users can interact with. These languages are often referred to as **frontend** languages because they are executed on the client side (in the user's browser).

### Courses to Learn HTML, CSS, and JavaScript:

- **Learning HTML and CSS**: [OpenClassrooms - Create Your Website with HTML5 and CSS3](https://openclassrooms.com/fr/courses/1603881-creez-votre-site-web-avec-html5-et-css3)
- **Learning JavaScript**: [OpenClassrooms - Learn to Code with JavaScript](https://openclassrooms.com/fr/courses/7696886-apprenez-a-programmer-avec-javascript)

### Useful Sites for CSS Customization:

- **Fonts**: [Google Fonts](https://fonts.google.com/)
- **Colors**: [Coolors](https://coolors.co/) or [W3Schools Color Picker](https://www.w3schools.com/colors/colors_picker.asp)
- **Color Gradients**: [UI Gradients](https://uigradients.com/#SeaBlizz)
- **Borders**: [CSS Border Generator](https://cssgenerator.org/border-css-generator.html) or [Fancy Border Radius](https://9elements.github.io/fancy-border-radius/)
- **Shadows**: [CSS Shadows Generator](https://shadows.brumm.af/) or [CSS Scan - Box Shadow Examples](https://getcssscan.com/css-box-shadow-examples)

In addition to client-side languages, websites also rely on server-side languages, often referred to as **backend frameworks**. While client-side languages control how a website looks and feels, server-side languages determine how the website behaves. Examples of server-side languages include PHP, Java, and Python. Backend frameworks, like Django for Python, are useful tools that streamline development and improve efficiency.

### How It All Connects:

1. **Client (User)** → **Request** → **Server (Backend Language, e.g., Python)**

   - The client, typically a user's web browser, initiates communication by sending a request to the server. This request could be for a specific web page, data, or an action to be performed (e.g., submitting a form).
   - The server, running a backend language such as Python, processes this request. Depending on the nature of the request, the server might execute various operations, including running scripts, querying a database, or performing calculations.

2. **Server** → **Response** → **Website (HTML/CSS/JavaScript)** → **Client**

   - After processing the request, the server generates a response. This response usually consists of HTML, CSS, and JavaScript code, which defines the structure, style, and behavior of the website.
   - The server sends this response back to the client's web browser, where it is rendered into a readable and interactive web page.
   - The web browser interprets the HTML to display the content, applies the CSS to style the page, and executes the JavaScript to enable dynamic features and interactivity.

### In More Complex Setups: Database Involvement

In many web applications, the server needs to access and manipulate data stored in a database to fulfill the client's request:

- **Database Access**: Before sending a response, the server often interacts with a database to retrieve, update, or delete data. This is common in websites with user accounts, content management systems, e-commerce platforms, and any application that requires persistent data storage.
  
- **SQL** is the most widely used language for managing and querying databases. The server uses SQL queries to interact with the database, retrieving information (like user profiles or product details) and incorporating it into the response sent to the client.

### Full Workflow Example:

1. **Client** (User logs in) → **Request** (Login details) → **Server** (Python)
2. **Server** → **Database** (Verify credentials) → **Server** (Prepare response)
3. **Server** → **Response** (User dashboard HTML/CSS/JavaScript) → **Client**

In this example, the server checks the login credentials against the database, and if valid, generates a personalized dashboard for the user, sending it back to the client's browser.

For more information, see: [Understanding the Web - OpenClassrooms](https://openclassrooms.com/fr/courses/1946386-comprendre-le-web)

A very usefull page: https://github.com/bradtraversy/design-resources-for-developers#html--css-templates

## How to deploy the website online ?

When creating and launching a website, three crucial components need to be considered: the domain name, hosting, and an FTP client.

### 1. Domain Name

- A **domain name** is the unique address where the website can be found on the internet (e.g., `www.example.com`). It’s essentially the website’s identity, making it easy for users to remember and access.
- Choosing the right domain name is important for branding and visibility.
- Domain names need to be registered through a domain registrar. Many web hosting services also offer domain registration as part of their packages.

### 2. Hosting

- **Web hosting** is a service that provides the technology and resources needed to store the website’s files and make them accessible on the internet. Without hosting, the website cannot be seen by others.
- There are different types of hosting services, including shared hosting (where multiple websites share the same server), VPS hosting (Virtual Private Server), and dedicated hosting (where a single server is dedicated to the website).

### 3. FTP Client

- An **FTP (File Transfer Protocol) client** is a software tool that allows you to transfer files between the local computer and the web server. This is essential for uploading the website files, including HTML, CSS, JavaScript, images, and other media, to the hosting server.
- **FileZilla** is a popular and user-friendly FTP client that supports secure file transfers (SFTP) and is widely used by web developers. It provides an intuitive interface for managing files on your server, making it easy to upload, download, or delete files as needed.
- FTP clients are especially useful when you need to update your website manually or when your website is not integrated with a content management system (CMS).

## Practical Steps to Get Started

- **Choosing a Domain and Host**: It’s often more convenient to purchase your domain name and hosting service from the same provider. This simplifies management and reduces the risk of technical issues. A reliable option is [OVH](https://www.ovhcloud.com/fr/web-hosting/), which offers both domain registration and hosting services in one place.

- **Using an FTP Client**: After setting up the domain and hosting, one can use an FTP client like FileZilla to transfer the website files to the server. This process involves connecting the FTP client to the hosting server using the credentials provided by the host (e.g., FTP address, username, and password).

For a comprehensive guide on how to put the website online, including details on domain registration, hosting, and using FTP clients, see this [OpenClassrooms course](https://openclassrooms.com/fr/courses/7192596-mettez-en-ligne-votre-site-web).

## Additional Resourcers

For additional resources, see the site from [MDN site](https://developer.mozilla.org/en-US/).
