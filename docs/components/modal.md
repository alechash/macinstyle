---
layout: default
title: Modal
parent: Components
---
# Modal
The Macinstyle modal is built to look like macOS Big Sur popups. The JavaScript to toggle the modals between visible and not visible is not included by default but a working example can be seen in the first example.

## Comparison

| macOS | Macinstyle |
|:---|:---|
| <img width="auto" src="/macinstyle/assets/images/macos-modal.png"> | <img width="auto" src="/macinstyle/assets/images/macinstyle-modal.png"> |

## Examples
Although we don't provide the JS to toggle the opening and closing of modals, there is an example below that includes the JavaScript. There is no need to include jQuery or any other JS library.

To toggle modals all you have to do is add/remove the `modal-hidden` class using JavaScript. To hide the modal again, all you have to do is add the `modal-hidden` class to the modal again.

An example of a modal is present here:
```html
<!-- button to open modal -->
<button onclick="openmodal()" class="btn button-secondary">open demo modal</button>

<!-- the modal itself -->
<div class="modal fade modal-hidden" id="modal">
    <div class="modal-content">
        <div class="modal-image">
            <img src="./testing/apple-logo.png">
        </div>
        <div class="modal-title">
            Are you sure you want to continue?
        </div>
        <div class="modal-body">
            Continuing will restart your computer
        </div>
        <div class="modal-footer">
            <button onclick="openmodal()" class="button-secondary btn">Cancel</button>
            <button onclick="openmodal()" class="button-primary btn">Continue</button>
        </div>
    </div>
</div>

<!-- the script to make the modal visible -->
<script>
    function openmodal() {
        var modal = document.getElementById('modal')
        modal.classList.toggle("modal-hidden");
    }
</script>
```

