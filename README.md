# Nitro SDK

> **C++ SDK to edit, render & convert PDFs.**  
> *With bindings for: C#, Java & GO.*

*🚨  This is an early, unreleased version of the Nitro SDK. It is available as-is and should not be redistributed.  
Contact us for more information: https://www.gonitro.com/about/contact.*

## Usage
A complete reference of the SDK can be found at https://github.com/nitro/sdk/wiki, but here's some quick examples:

### Edit
```cpp
auto doc = nitro::sdk::open("my_doc.pdf");
auto page = doc.get_page(0);
page.add_image("my_image.png", {0, 256, 256, 0}));
```

### Render
```cpp
auto doc = nitro::sdk::open("my_doc.pdf");
doc.get_page(0).view().render("my_doc_rendered.png");
```

### Convert
```cpp
nitro::sdk::pdf_to_pdfa("my_doc.pdf", "my_doc.pdfa");
```
