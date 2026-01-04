# Annotator
Client-side web application for annotating HTML documents with colored highlights, tags, and explanations. Import and Export HTML and associated JSON. 

### 🚀 Getting started
* Clone the repository or download the source:
```bash
git clone https://github.com/your-username/simple-html-annotator.git
```
* Open the annotator.html file directly in your browser.
* No installation is required. 

### 🧭 Usage
* Import an HTML file using the file selector in the left options pane
* Select text in the right document pane
* Select a highlight color
* Add tag/topic and explanation
* Click the ```Add Highlight from Selection``` button
* Click the highlighted text in the document pane or the list of tags in the options pane to edit or delete
* Export JSON when finished
* Import the HTML and associted JSON again to restore highlights

### 📤 Export Format
Annotations are stored in JSON and anchored with XPath and character offsets. An example format is as follows:

```
{
  "version": 1,
  "createdAt": "2026-01-02T21:45:00.000Z",
  "htmlFingerprint": "a1b2c3d4",
  "annotations": [
    {
      "id": "uuid",
      "color": "#fde68a",
      "tag": "Claim",
      "note": "Main argument of the paragraph",
      "startXPath": "./p[3]::text()[1]",
      "startOffset": 15,
      "endXPath": "./p[3]::text()[1]",
      "endOffset": 64,
      "snippet": "This paper argues that..."
    }
  ]
}
```

### ⚠️ Notes
* Overlapping highlight is not yet supported
* Annotation anchoring may fail if the HTML structure or text changes significantly
* Only use trusted HTML files. We remove scripts and inline event handlers, but this is not a full security sanitizer.

### 📄 License 
MIT License. Feel free to use, modify, and adapt for research or educational purposes. 
