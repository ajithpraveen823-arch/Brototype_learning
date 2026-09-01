# 🌐✨ Understand the Basics of HTML

> 🚀 **HTML = HyperText Markup Language**
> HTML is the **standard language used to create the structure of web pages**.

### 🧠 Think of a Website Like a House

```text
🏠 Website
│
├── 🧱 HTML       → Structure
├── 🎨 CSS        → Design & Styling
└── ⚡ JavaScript → Logic & Interactivity
```

---

# 📄 1. HTML Document Structure

Every HTML page follows a basic structure:

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Web Page</title>
</head>

<body>
    <h1>Welcome to My Website</h1>
    <p>This is my first HTML page.</p>
</body>
</html>
```

### 🔍 Understanding Each Part

| Tag               | Purpose                      |
| ----------------- | ---------------------------- |
| `<!DOCTYPE html>` | 📢 Declares HTML5            |
| `<html>`          | 🌐 Root of the document      |
| `<head>`          | ⚙️ Contains page information |
| `<title>`         | 🏷️ Sets browser tab title   |
| `<body>`          | 👀 Contains visible content  |

---

## 🟡 `<!DOCTYPE html>`

Tells the browser that the document uses **HTML5**.

```html
<!DOCTYPE html>
```

---

## 🌐 `<html>`

The root element of the entire HTML document.

```html
<html>
    ...
</html>
```

---

## ⚙️ `<head>`

Contains information about the webpage that is generally not displayed directly.

```html
<head>
    <title>My Website</title>
</head>
```

Common elements:

```text
<meta>   → Page metadata
<title>  → Page title
<link>   → External resources
<style>  → CSS
<script> → JavaScript
```

---

## 👀 `<body>`

Contains everything that appears on the webpage.

```html
<body>
    <h1>Hello World!</h1>
    <p>Welcome to my website.</p>
</body>
```

---

# 🧩 2. Common HTML Elements

## 🏆 Headings

HTML provides **6 heading levels**:

```html
<h1>Main Heading</h1>
<h2>Sub Heading</h2>
<h3>Section Heading</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

### 📊 Heading Hierarchy

```text
<h1> ⭐⭐⭐⭐⭐⭐
   ↓
<h2> ⭐⭐⭐⭐⭐
   ↓
<h3> ⭐⭐⭐⭐
   ↓
<h4> ⭐⭐⭐
   ↓
<h5> ⭐⭐
   ↓
<h6> ⭐
```

💡 Use headings according to their **meaning and document structure**, not simply to make text bigger.

---

## 📝 Paragraph

The `<p>` tag is used for paragraphs.

```html
<p>
    HTML is used to create the structure of web pages.
</p>
```

---

## 🔗 Links

The `<a>` tag creates hyperlinks.

```html
<a href="https://www.google.com">
    Visit Google
</a>
```

Here:

```text
<a>      → Link element
href     → Destination
```

---

## 🖼️ Images

The `<img>` tag displays images.

```html
<img src="photo.jpg" alt="My Photo">
```

### 🔑 Important Attributes

```text
src → 📁 Image location
alt → ♿ Alternative description
```

---

# ⚙️ 3. HTML Attributes

### 💡 What is an Attribute?

An **attribute provides additional information** about an HTML element.

### Basic Syntax

```html
<tag attribute="value">
```

Example:

```html
<a href="https://example.com">
    Visit Website
</a>
```

Here:

```text
href = attribute
https://example.com = value
```

---

## 🔗 `href`

Used with `<a>` to specify the destination.

```html
<a href="https://example.com">
    Open Website
</a>
```

---

## 🖼️ `src`

Specifies the source/location of an image.

```html
<img src="profile.jpg">
```

---

## ♿ `alt`

Provides alternative text for an image.

```html
<img 
    src="cat.jpg" 
    alt="A cute cat">
```

### Why is `alt` important?

✅ Accessibility
✅ Helps describe images
✅ Appears when an image cannot load
✅ Helps screen readers understand the image

---

## 💬 `title`

Provides additional information, commonly displayed as a tooltip when hovering.

```html
<p title="This is additional information">
    Hover over me
</p>
```

---

# 🧠 4. Semantic HTML

## 🟢 What is a Semantic Tag?

A **semantic tag clearly describes the meaning of its content**.

### ⭐ Examples

```html
<header>Header</header>

<nav>Navigation</nav>

<main>Main Content</main>

<section>Section</section>

<article>Article</article>

<aside>Sidebar</aside>

<footer>Footer</footer>
```

---

## 🏷️ Common Semantic Tags

| Tag         | Meaning                    |
| ----------- | -------------------------- |
| `<header>`  | 📰 Header                  |
| `<nav>`     | 🧭 Navigation              |
| `<main>`    | 📄 Main content            |
| `<section>` | 📦 Section                 |
| `<article>` | 📝 Independent content     |
| `<aside>`   | 📌 Related/sidebar content |
| `<footer>`  | 🔻 Footer                  |

### Example

```html
<header>
    <h1>My Website</h1>
</header>

<nav>
    <a href="#">Home</a>
    <a href="#">About</a>
</nav>

<main>
    <section>
        <h2>About Me</h2>
        <p>I am learning web development.</p>
    </section>
</main>

<footer>
    <p>© 2026 My Website</p>
</footer>
```

---

# 🔴 5. Non-Semantic Tags

Non-semantic tags **do not tell us what their content means**.

The most common are:

### 📦 `<div>`

A general block-level container.

```html
<div>
    <h2>About Me</h2>
    <p>I am learning HTML.</p>
</div>
```

### ✏️ `<span>`

A general inline container.

```html
<p>
    I am learning 
    <span>HTML</span>.
</p>
```

---

# ⚔️ Semantic vs Non-Semantic

| 🟢 Semantic | 🔴 Non-Semantic |
| ----------- | --------------- |
| `<header>`  | `<div>`         |
| `<nav>`     | `<span>`        |
| `<main>`    |                 |
| `<section>` |                 |
| `<article>` |                 |
| `<aside>`   |                 |
| `<footer>`  |                 |

### 🧠 Easy Trick

> **Semantic = Meaningful 🟢**

```text
<header>  → "This is a header"
<nav>     → "This is navigation"
<article> → "This is an article"
<footer>  → "This is a footer"
```

> **Non-Semantic = General Container 🔴**

```text
<div>  → General block
<span> → General inline content
```

---

# 🚀 6. Complete HTML Example

```html
<!DOCTYPE html>

<html>

<head>
    <title>My Portfolio</title>
</head>

<body>

    <!-- Header -->
    <header>
        <h1>👨‍💻 My Portfolio</h1>
        <p>Welcome to my website!</p>
    </header>

    <!-- Navigation -->
    <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
    </nav>

    <!-- Main Content -->
    <main>

        <section id="about">

            <h2>🙋 About Me</h2>

            <p>
                I am learning HTML and web development.
            </p>

            <img 
                src="profile.jpg"
                alt="My profile photo"
                title="My Profile Photo"
            >

        </section>

        <section id="skills">

            <h2>💻 My Skills</h2>

            <p>HTML, CSS and JavaScript</p>

        </section>

    </main>

    <!-- Footer -->
    <footer>
        <p>© 2026 My Portfolio</p>
    </footer>

</body>

</html>
```

---

# 🗺️ 7. HTML Structure at a Glance

```text
🌐 HTML DOCUMENT
│
├── 📢 <!DOCTYPE html>
│
├── 🌐 <html>
│   │
│   ├── ⚙️ <head>
│   │   └── 🏷️ <title>
│   │
│   └── 👀 <body>
│       │
│       ├── 📰 <header>
│       ├── 🧭 <nav>
│       ├── 📄 <main>
│       │   ├── 📦 <section>
│       │   └── 📝 <article>
│       └── 🔻 <footer>
```

---

# 🎯 Quick Revision

### 📌 Document Structure

```text
<!DOCTYPE html> → HTML5
<html>          → Root
<head>          → Information
<body>          → Visible content
```

### 📌 Common Elements

```text
<h1> → Heading
<p>  → Paragraph
<a>  → Link
<img> → Image
```

### 📌 Attributes

```text
href  → 🔗 Link destination
src   → 🖼️ Source
alt   → ♿ Alternative text
title → 💬 Extra information
```

### 📌 Tags

```text
🟢 Semantic
<header> <nav> <main> <section> <article> <footer>

🔴 Non-Semantic
<div> <span>
```

---

## 🏆 Remember This!

> **HTML = Structure 🧱**
> **CSS = Style 🎨**
> **JavaScript = Behavior ⚡**

**HTML is the foundation of web development.** 🚀
