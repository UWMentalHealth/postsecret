---
title: Test Series

resources:

- src: mypicture.jpg
  name: "This is my test image title"
  params:
    order: 1
    description: Photo description. If you want to add your own link, specify button_text and button_url here.
    button_text: Links to resources
    button_url: "https://www.google.com"

- src: mysecondpicture.jpg
  name: "Explicit image"
  params:
    order: 2
    explicit: true
    warning: "This image contains sensitive content"
    description: Photo description. If you want to add your own link, specify button_text and button_url here.
    button_text: Links to resources
    button_url: "https://www.google.com"

---