### WordPress Notes

***

#### HEADER

* `<?php wp_head(); ?>` should be inside `header.php` just before your closing tag `</head>`
* if you include opening `<div>` tag, make sure you close it inside footer

***

#### FOOTER

* `<?php wp_footer(); ?>` comes right before the closing body tag `</body>`
* if you included opening tags in `header.php` make sure you inlcude the closing tag inside `footer.php`
