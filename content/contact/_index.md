---
title: "Contact"
featured_image: "images/contact.jpg"
---


Do get in touch!

{{< form-contact action="https://formspree.io/f/mzzbqebg" >}}

{{< rawhtml >}}
  <script>
    const form = document.querySelector('form');
    form.addEventListener('submit', e => {
        e.preventDefault();
        const formData = new FormData(form);
        const xhr = new XMLHttpRequest();
        xhr.open('POST', form.action, true);
        xhr.setRequestHeader('Accept', 'application/json');
        xhr.onreadystatechange = () => {
            if (xhr.readyState !== XMLHttpRequest.DONE) return;
            if (xhr.status === 200) {
                form.reset();
                alert('Thank you for your message.');
            } else {
                alert('Sorry, there was an error. Please try again later.');
            }
        };
        xhr.send(formData);
    });
</script>
{{< /rawhtml >}}
