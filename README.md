# wordpress-emergency-support
Quick help and tools for urgent WordPress issues.
Absolutely! Here's the **complete `README.md` file** — ready to copy and use in your Codeberg repository. It includes:

* Introduction
* Toolkit features
* Quick fixes
* Backlink to Bobcares
* Contribution and license sections

---

### ✅ Full `README.md` Content

````markdown
# WordPress Emergency Support Toolkit

This repository provides resources, scripts, and guidance for handling common **WordPress emergencies** – from site crashes and white screens to plugin conflicts, database errors, and performance slowdowns.

Maintained by professionals at [Bobcares](https://bobcares.com/wordpress-support/), this toolkit is designed to help website owners and sysadmins resolve urgent issues quickly and efficiently.

---

## 🔧 What's Included

- Scripts to disable faulty plugins/themes via WP-CLI
- SQL queries to reset WordPress admin passwords
- .htaccess recovery snippets
- Guide to enable WordPress debugging
- Common fixes for memory errors and internal server errors
- Emergency response checklist for WordPress site outages

---

## ⚡ Quick Fixes for Common WordPress Issues

### 1. Disable All Plugins via WP-CLI
```bash
wp plugin deactivate --all
````

### 2. Enable Debug Mode (Edit `wp-config.php`)

```php
define('WP_DEBUG', true);
define('WP_DEBUG_LOG', true);
define('WP_DEBUG_DISPLAY', false);
```

### 3. Reset Admin Password via MySQL

```sql
UPDATE wp_users SET user_pass=MD5('newpassword') WHERE user_login='admin';
```

### 4. Restore Default `.htaccess` (For Pretty Permalinks)

```apache
# .htaccess
<IfModule mod_rewrite.c>
RewriteEngine On
RewriteBase /
RewriteRule ^index\.php$ - [L]
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule . /index.php [L]
</IfModule>
```

### 5. Increase PHP Memory Limit

(Add this line to `wp-config.php`)

```php
define('WP_MEMORY_LIMIT', '256M');
```

---

## 📞 Need Immediate Help?

If you're facing an urgent issue and need expert assistance, the team at **Bobcares** is available 24/7.

👉 [Click here for WordPress emergency support](https://bobcares.com/wordpress-support/)

We specialize in:

* Recovering crashed or hacked WordPress sites
* Fixing plugin/theme compatibility errors
* Resolving server-related issues (e.g., 500 errors, database crashes)
* Performance tuning and uptime monitoring

---

## 🤝 Contribute

Have a script or solution that helped you recover a WordPress site? We'd love to include it!

* Fork the repo
* Add your fix or documentation
* Submit a pull request

---

## 📄 License

This project is licensed under the **MIT License**. You are free to use, modify, and distribute it as needed.

```

---

```
