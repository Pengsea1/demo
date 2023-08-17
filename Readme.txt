Testing git
// HTML
<input type="email" id="email-input" value="example@example.com">
<button id="copy-button">Copy</button>
<div id="message"></div>

// jQuery
$(document).ready(function() {
  $("#copy-button").click(function() {
    var email = $("#email-input").val(); // get the email value
    navigator.clipboard.writeText(email) // write it to the clipboard
      .then(function() {
        $("#message").text("Email copied!"); // show success message
      })
      .catch(function() {
        $("#message").text("Copy failed!"); // show error message
      });
  });
});
