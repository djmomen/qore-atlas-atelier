# Qore Atlas Atelier

Coming-soon website for Qore Atlas Atelier, with original concept imagery and a scroll-driven architectural presentation.

## Hosting with aaPanel

This is a static website. No installation, build command, PHP runtime, Node.js process or database is required.

1. Point your domain's DNS A record to the aaPanel server's public IP.
2. In aaPanel, choose **Website → Add site → Create for Git**.
3. Select this repository and the **main** branch.
4. Clone into an empty directory such as `/www/wwwroot/your-domain`.
5. Select **Static / Pure static** if the PHP selector offers it.
6. After creation, open the site's **Site directory** settings and set **Running directory** to **/dist**. The public document root must be `/www/wwwroot/your-domain/dist`.
7. Keep `index.html` as the default document. Enable SSL and HTTPS after DNS is resolving to the server.

There is no build step for subsequent deployments. Pull updates to `main`, or configure aaPanel's Git Manager webhook to pull new commits automatically. Keep webhook TLS verification enabled and use a valid HTTPS certificate.

## Local preview

```sh
python3 -m http.server 4173 --directory dist
```

Open http://localhost:4173/.

## Files

- `dist/index.html`: page content and structure
- `dist/style.css`: responsive styling and static fallback
- `dist/script.js`: scroll scenes and local signup preview
- `dist/assets/`: images, original monogram and locally hosted DM Sans font
- `ASSETS.md`: image descriptions and font license details

## Launch-list status

The email form is a prototype: it saves an email only in the visitor's browser and does not send emails or create a real mailing-list subscription. Connect a mailing-list provider before using it for launch notifications.

## Accessibility and motion

The website includes native scrolling, keyboard navigation, visible focus, reduced-motion support and a static fallback when JavaScript is disabled. Physical-device and cross-browser performance should be checked before a public launch.

## Assets

Images are original AI-generated design concepts; they do not depict completed projects. DM Sans is distributed under its bundled SIL Open Font License. See `dist/assets/DM-Sans-LICENSE.txt`.
