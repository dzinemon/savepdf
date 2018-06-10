# Save PDF

on github pages - [link](https://dzinemon.github.io/savepdf/)

using: [jsPDF](https://github.com/MrRio/jsPDF)

```javascript

var saveBtn = document.getElementById('saveBtn');
var saveArea = document.getElementById('save-pdf');

saveBtn.addEventListener('click', function() {
  var pdf = new jsPDF('p', 'mm', 'a4');

  var options = {
    pagesplit: true,
    background: '#FFFFFF',
    width: saveArea.offsetWidth,
    height: saveArea.offsetHeight
  };

  pdf.addHTML(saveArea, options, function() {
    pdf.save('TestPdf.pdf');
  });
});

```