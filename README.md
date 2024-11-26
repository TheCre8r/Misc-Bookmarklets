# Misc-Bookmarklets


## Vance County Register of Deeds

### Plat
```js
javascript:(function(){var input=prompt("Enter the code (e.g., A1, Z-101b):");if(input){var match=/^([a-zA-Z])(-?(\d+))(.*)$/.exec(input.trim());if(match){var letter=match[1].toLowerCase();var number=match[3].padStart(4,'0');var suffix=match[4];var instrument=letter+number+suffix;var url="https://www.vancencrod.org/DocumentView.asp?DocumentType=Plat&Instrument=000"+instrument+"&ReturnTo=BookAndPage.asp";window.open(url,"_blank");}else{alert("Invalid format. Please enter a valid code.");}}})();
```

### Deed
```js
javascript:(function(){var input=prompt("Enter the book and page (e.g., Book 552 Page 0258, 552 258):");if(input){var match=input.match(/(?:Book[:\s]*|B\s*)?(\d+)\s*(?:Page[:\s]*|Pg\s*|P\s*)?(\d+)/i);if(match){var book=match[1].padStart(4,'0');var page=match[2].padStart(4,'0');var instrument=book+page;var url="https://www.vancencrod.org/DocumentView.asp?DocumentType=Deeds&Instrument="+instrument+"&ReturnTo=BookAndPage.asp";window.open(url,"_blank");}else{alert("Invalid format. Please enter a valid book and page.");}}})();
```
