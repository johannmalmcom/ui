# ui

```php

require_once("./vendor/autoload.php");

use UI\Tag;

// Titles
echo Tag::title("Title 1", 1);
echo Tag::title("Title 2", 2);
echo Tag::title("Title 3", 3);
echo Tag::title("Title 4", 4);
echo Tag::title("Title 5", 5);
echo Tag::title("Title 6", 6);

// Paragraph
echo Tag::paragraph("Paragraph");

// Link
echo Tag::anchor("Anchor", "#");

// Image
echo Tag::image("Image", "/image.jpg");

// Divider
echo Tag::divider(
    Tag::title("Title 1", 1).
    Tag::paragraph("Paragraph").
    Tag::anchor("Anchor", "#")
);

// Form
echo Tag::form(
    Tag::inputText("textfield", "Text Field", $_POST["textField"] ?? "").
    Tag::inputPassword("passwordfield", "Password Field", $_POST["passwordfield"] ?? "").
    Tag::inputFile("filefield", "File Field", $_POST["filefield"] ?? "").
    Tag::inputTextarea("textareafield", "Textarea Field", $_POST["textareafield"] ?? "").
    Tag::buttonSubmit("Submit")
, "/action");

// Button 
echo Tag::button("Button", "#");

// Various
echo Tag::general("video", [
    "src" => "video.mov"
]);

```