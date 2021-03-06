---
id: cdn-links
title: CDN Links
permalink: docs/cdn-links.html
prev: create-a-new-react-app.html
next: hello-world.html
---

Τόσο το React όσο και το ReactDOM είναι διαθέσιμα μέσω CDN.

```html
<script crossorigin src="https://unpkg.com/react@16/umd/react.development.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
```

Οι παραπάνω εκδόσεις προορίζονται μόνο για ανάπτυξη (Development) και δεν είναι κατάλληλες για παραγωγή (Production). Ελαχιστοποιημένες (Minified) και βελτιστοποιημένες (Optimized) εκδόσεις παραγωγής (Production) του React διατίθενται στη διεύθυνση:

```html
<script crossorigin src="https://unpkg.com/react@16/umd/react.production.min.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@16/umd/react-dom.production.min.js"></script>
```

Για να φορτώσετε μια συγκεκριμένη έκδοση του `react` και `react-dom`, αντικαταστήστε το `16` με τον αριθμό έκδοσης.

### Γιατί το `crossorigin` χαρακτηριστικό (Attribute)? {#why-the-crossorigin-attribute}

Εάν χρησιμοποιείτε το React μέσω CDN, σας συνιστούμε να διατηρήσετε το [`crossorigin`](https://developer.mozilla.org/en-US/docs/Web/HTML/CORS_settings_attributes) σύνολο χαρακτηριστικών:

```html
<script crossorigin src="..."></script>
```

Συνιστούμε επίσης να επαληθεύσετε ότι το CDN που χρησιμοποιείτε ορίζει την `Access-Control-Allow-Origin: *` κεφαλίδα HTTP:

![Access-Control-Allow-Origin: *](../images/docs/cdn-cors-header.png)

Αυτό επιτρέπει μία καλύτερη [εμπειρία χειρισμού σφαλμάτων](/blog/2017/07/26/error-handling-in-react-16.html) στο React 16 και για μεταγενέστερες εκδόσεις.
