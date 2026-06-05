<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Privacy Policy – Scanner: PDF Documents</title>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg: #ffffff;
      --bg-secondary: #f7f7f5;
      --text-primary: #1a1a1a;
      --text-secondary: #555551;
      --text-tertiary: #999994;
      --border: rgba(0,0,0,0.1);
      --border-strong: rgba(0,0,0,0.18);
      --accent: #3B6D11;
      --radius-md: 8px;
      --radius-lg: 12px;
    }

    @media (prefers-color-scheme: dark) {
      :root {
        --bg: #1a1a18;
        --bg-secondary: #242422;
        --text-primary: #f0ede8;
        --text-secondary: #a8a49e;
        --text-tertiary: #6b6864;
        --border: rgba(255,255,255,0.1);
        --border-strong: rgba(255,255,255,0.18);
        --accent: #97C459;
      }
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
      background: var(--bg);
      color: var(--text-primary);
      line-height: 1.7;
      font-size: 16px;
      padding: 0 1rem;
    }

    .container {
      max-width: 720px;
      margin: 0 auto;
      padding: 3rem 0 4rem;
    }

    /* lang toggle */
    .lang-bar {
      display: flex;
      gap: 6px;
      margin-bottom: 2rem;
    }
    .lang-btn {
      font-size: 13px;
      padding: 5px 14px;
      border: 0.5px solid var(--border-strong);
      border-radius: var(--radius-md);
      background: transparent;
      color: var(--text-secondary);
      cursor: pointer;
      font-family: inherit;
      transition: background 0.15s, color 0.15s;
    }
    .lang-btn.active {
      background: var(--bg-secondary);
      color: var(--text-primary);
      font-weight: 500;
    }

    /* header */
    .pp-header {
      margin-bottom: 2.25rem;
      padding-bottom: 1.75rem;
      border-bottom: 0.5px solid var(--border);
    }
    .app-badge {
      display: inline-flex;
      align-items: center;
      gap: 7px;
      background: var(--bg-secondary);
      border: 0.5px solid var(--border);
      border-radius: var(--radius-md);
      padding: 5px 12px;
      font-size: 13px;
      color: var(--text-secondary);
      margin-bottom: 1rem;
    }
    .app-badge svg { width: 15px; height: 15px; flex-shrink: 0; }
    h1 {
      font-size: 26px;
      font-weight: 600;
      color: var(--text-primary);
      margin-bottom: 0.4rem;
      letter-spacing: -0.3px;
    }
    .meta {
      font-size: 13px;
      color: var(--text-tertiary);
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    /* sections */
    .section { margin-bottom: 2rem; }
    .section-title {
      font-size: 15px;
      font-weight: 600;
      color: var(--text-primary);
      margin-bottom: 0.75rem;
      display: flex;
      align-items: center;
      gap: 8px;
    }
    .section-title svg { width: 17px; height: 17px; color: var(--text-tertiary); flex-shrink: 0; }

    p, .body-text {
      font-size: 14.5px;
      color: var(--text-secondary);
      line-height: 1.75;
    }
    p + p { margin-top: 0.6rem; }

    ul {
      list-style: none;
      margin-top: 0.6rem;
      display: flex;
      flex-direction: column;
      gap: 6px;
    }
    ul li {
      font-size: 14.5px;
      color: var(--text-secondary);
      padding-left: 1.2rem;
      position: relative;
      line-height: 1.65;
    }
    ul li::before { content: "–"; position: absolute; left: 0; color: var(--text-tertiary); }

    /* permission grid */
    .permission-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 10px;
      margin-top: 0.75rem;
    }
    .permission-card {
      background: var(--bg-secondary);
      border: 0.5px solid var(--border);
      border-radius: var(--radius-md);
      padding: 12px 14px;
    }
    .permission-label {
      font-size: 13px;
      font-weight: 600;
      color: var(--text-primary);
      margin-bottom: 5px;
      display: flex;
      align-items: center;
      gap: 7px;
    }
    .permission-label svg { width: 15px; height: 15px; color: var(--text-tertiary); }
    .permission-desc {
      font-size: 12.5px;
      color: var(--text-secondary);
      line-height: 1.6;
    }

    /* callout */
    .callout {
      background: var(--bg-secondary);
      border-left: 2px solid var(--border-strong);
      border-radius: 0 var(--radius-md) var(--radius-md) 0;
      padding: 12px 16px;
      margin-top: 0.75rem;
      font-size: 14px;
      color: var(--text-secondary);
      line-height: 1.65;
    }

    /* contact */
    .contact-row {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 14px;
      color: var(--text-secondary);
      margin-top: 8px;
    }
    .contact-row svg { width: 16px; height: 16px; color: var(--text-tertiary); flex-shrink: 0; }
    .contact-row a { color: var(--text-secondary); text-decoration: underline; text-underline-offset: 3px; }

    hr {
      border: none;
      border-top: 0.5px solid var(--border);
      margin: 1.75rem 0;
    }

    footer {
      margin-top: 2.5rem;
      padding-top: 1.5rem;
      border-top: 0.5px solid var(--border);
      text-align: center;
      font-size: 12px;
      color: var(--text-tertiary);
      line-height: 1.7;
    }

    [lang-content] { display: none; }
    [lang-content].active { display: block; }
  </style>
</head>
<body>
<div class="container">

  <div class="lang-bar">
    <button class="lang-btn active" onclick="setLang('en', this)">English</button>
    <button class="lang-btn" onclick="setLang('tr', this)">Türkçe</button>
  </div>

  <!-- ─── ENGLISH ─────────────────────────────────────────────── -->
  <div lang-content="en" class="active">

    <div class="pp-header">
      <div class="app-badge">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="3" width="18" height="18" rx="2"/><path d="M7 7h10M7 12h10M7 17h6"/></svg>
        Scanner: PDF Documents
      </div>
      <h1>Privacy Policy</h1>
      <div class="meta">
        <span>Effective date: June 5, 2025</span>
        <span>Last updated: June 5, 2025</span>
      </div>
    </div>

    <div class="section">
      <div class="section-title">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><line x1="12" y1="16" x2="12" y2="12"/><line x1="12" y1="8" x2="12.01" y2="8"/></svg>
        Overview
      </div>
      <p>Scanner: PDF Documents ("we", "our", or "the app") is committed to protecting your privacy. This Privacy Policy explains how we handle information when you use our mobile application.</p>
      <p>We built this app with a privacy-first approach. Your scanned documents stay on your device. We do not sell your data, and we do not show ads.</p>
    </div>

    <hr>

    <div class="section">
      <div class="section-title">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>
        Permissions we request
      </div>
      <p>The app requests access to the following device features:</p>
      <div class="permission-grid">
        <div class="permission-card">
          <div class="permission-label">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M23 19a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h4l2-3h6l2 3h4a2 2 0 0 1 2 2z"/><circle cx="12" cy="13" r="4"/></svg>
            Camera
          </div>
          <div class="permission-desc">Used to capture photos of documents for scanning. All processing is done locally on your device.</div>
        </div>
        <div class="permission-card">
          <div class="permission-label">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
            Photo library
          </div>
          <div class="permission-desc">Used to import existing images from your gallery for scanning. Supports selecting multiple images at once.</div>
        </div>
        <div class="permission-card">
          <div class="permission-label">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><circle cx="18" cy="5" r="3"/><circle cx="6" cy="12" r="3"/><circle cx="18" cy="19" r="3"/><line x1="8.59" y1="13.51" x2="15.42" y2="17.49"/><line x1="15.41" y1="6.51" x2="8.59" y2="10.49"/></svg>
            Sharing
          </div>
          <div class="permission-desc">Allows you to export scanned documents as PDFs or images using the iOS system share sheet.</div>
        </div>
        <div class="permission-card">
          <div class="permission-label">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><ellipse cx="12" cy="5" rx="9" ry="3"/><path d="M21 12c0 1.66-4 3-9 3s-9-1.34-9-3"/><path d="M3 5v14c0 1.66 4 3 9 3s9-1.34 9-3V5"/></svg>
            Local storage
          </div>
          <div class="permission-desc">Documents, settings, and preferences are stored locally on your device using Hive. No data leaves your device.</div>
        </div>
      </div>
    </div>

    <hr>

    <div class="section">
      <div class="section-title">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="16" y1="13" x2="8" y2="13"/><line x1="16" y1="17" x2="8" y2="17"/><polyline points="10 9 9 9 8 9"/></svg>
        Information we collect
      </div>
      <p>We collect the minimum information needed to operate the app's features:</p>
      <ul>
        <li>Scanned documents and images — stored only on your device, never uploaded to our servers.</li>
        <li>App preferences and settings — stored locally on your device.</li>
        <li>Translation requests — when you use the translation feature, the extracted text is sent to a third-party translation service over an encrypted (HTTPS) connection. We do not store or log this data.</li>
      </ul>
      <div class="callout">
        We do not collect your name, email address, phone number, location, or any other personally identifying information.
      </div>
    </div>

    <hr>

    <div class="section">
      <div class="section-title">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
        Third-party services
      </div>
      <p>The app uses one external service:</p>
      <ul>
        <li><strong>Translation service</strong> — When you translate text extracted from a scanned document, that text is transmitted to an external translation API over HTTPS. This is necessary for the feature to function. The translation provider may have its own data retention practices; please review their privacy policy.</li>
      </ul>
      <p style="margin-top: 0.75rem;">No analytics, advertising, or tracking SDKs are included in the app.</p>
    </div>

    <hr>

    <div class="section">
      <div class="section-title">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="11" width="18" height="11" rx="2" ry="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>
        Data security
      </div>
      <p>Your documents and data are stored locally on your device. We have no access to your scanned documents. Files shared via the system share sheet are transferred only to apps you explicitly choose.</p>
      <p>We recommend keeping your device software up to date to benefit from the latest operating system security protections.</p>
    </div>

    <hr>

    <div class="section">
      <div class="section-title">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg>
        Children's privacy
      </div>
      <p>This app is not directed at children under the age of 13. We do not knowingly collect personal information from children. If you believe a child has provided personal data through the app, please contact us and we will take appropriate action.</p>
    </div>

    <hr>

    <div class="section">
      <div class="section-title">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><polyline points="23 4 23 10 17 10"/><polyline points="1 20 1 14 7 14"/><path d="M3.51 9a9 9 0 0 1 14.85-3.36L23 10M1 14l4.64 4.36A9 9 0 0 0 20.49 15"/></svg>
        Changes to this policy
      </div>
      <p>We may update this Privacy Policy from time to time. When we do, we will update the "Last updated" date at the top of this page. Continued use of the app after any changes constitutes your acceptance of the updated policy.</p>
    </div>

    <hr>

    <div class="section">
      <div class="section-title">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        Contact us
      </div>
      <p>If you have any questions about this Privacy Policy, please contact us:</p>
      <div class="contact-row">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        <a href="mailto:support@yourapp.com">support@yourapp.com</a>
      </div>
      <div class="contact-row">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
        <a href="https://yourapp.com/privacy">yourapp.com/privacy</a>
      </div>
    </div>

    <footer>
      <p>This privacy policy was prepared for Scanner: PDF Documents.<br>
      © 2025 Your Company Name. All rights reserved.</p>
    </footer>

  </div>

  <!-- ─── TÜRKÇE ─────────────────────────────────────────────── -->
  <div lang-content="tr">

    <div class="pp-header">
      <div class="app-badge">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="3" width="18" height="18" rx="2"/><path d="M7 7h10M7 12h10M7 17h6"/></svg>
        Scanner: PDF Documents
      </div>
      <h1>Gizlilik Politikası</h1>
      <div class="meta">
        <span>Yürürlük tarihi: 5 Haziran 2025</span>
        <span>Son güncelleme: 5 Haziran 2025</span>
      </div>
    </div>

    <div class="section">
      <div class="section-title">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><line x1="12" y1="16" x2="12" y2="12"/><line x1="12" y1="8" x2="12.01" y2="8"/></svg>
        Genel bakış
      </div>
      <p>Scanner: PDF Documents ("biz", "uygulama") olarak gizliliğinizi korumayı taahhüt ediyoruz. Bu Gizlilik Politikası, mobil uygulamamızı kullandığınızda bilgilerinizi nasıl işlediğimizi açıklar.</p>
      <p>Bu uygulamayı gizlilik öncelikli bir yaklaşımla geliştirdik. Taranan belgeleriniz cihazınızda kalır. Verilerinizi satmıyor, reklam göstermiyoruz.</p>
    </div>

    <hr>

    <div class="section">
      <div class="section-title">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>
        Talep ettiğimiz izinler
      </div>
      <p>Uygulama, aşağıdaki cihaz özelliklerine erişim talep eder:</p>
      <div class="permission-grid">
        <div class="permission-card">
          <div class="permission-label">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M23 19a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h4l2-3h6l2 3h4a2 2 0 0 1 2 2z"/><circle cx="12" cy="13" r="4"/></svg>
            Kamera
          </div>
          <div class="permission-desc">Belgelerin taranması için fotoğraf çekiminde kullanılır. Tüm işlemler cihazınızda yerel olarak gerçekleşir.</div>
        </div>
        <div class="permission-card">
          <div class="permission-label">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
            Fotoğraf galerisi
          </div>
          <div class="permission-desc">Mevcut görüntüleri galerinizden alarak tarama için kullanılır. Çoklu görsel seçimini destekler.</div>
        </div>
        <div class="permission-card">
          <div class="permission-label">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><circle cx="18" cy="5" r="3"/><circle cx="6" cy="12" r="3"/><circle cx="18" cy="19" r="3"/><line x1="8.59" y1="13.51" x2="15.42" y2="17.49"/><line x1="15.41" y1="6.51" x2="8.59" y2="10.49"/></svg>
            Paylaşım
          </div>
          <div class="permission-desc">Taranan belgeleri PDF veya görüntü olarak iOS sistem paylaşım sayfasıyla dışa aktarmanıza olanak tanır.</div>
        </div>
        <div class="permission-card">
          <div class="permission-label">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><ellipse cx="12" cy="5" rx="9" ry="3"/><path d="M21 12c0 1.66-4 3-9 3s-9-1.34-9-3"/><path d="M3 5v14c0 1.66 4 3 9 3s9-1.34 9-3V5"/></svg>
            Yerel depolama
          </div>
          <div class="permission-desc">Belgeler, ayarlar ve tercihler Hive ile cihazınızda yerel olarak saklanır. Herhangi bir veri cihazı terk etmez.</div>
        </div>
      </div>
    </div>

    <hr>

    <div class="section">
      <div class="section-title">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="16" y1="13" x2="8" y2="13"/><line x1="16" y1="17" x2="8" y2="17"/><polyline points="10 9 9 9 8 9"/></svg>
        Topladığımız bilgiler
      </div>
      <p>Yalnızca uygulamanın işlevlerini sunmak için gereken minimum bilgiyi toplarız:</p>
      <ul>
        <li>Taranan belgeler ve görüntüler — yalnızca cihazınızda saklanır, sunucularımıza yüklenmez.</li>
        <li>Uygulama tercihleri ve ayarları — cihazınızda yerel olarak saklanır.</li>
        <li>Çeviri istekleri — çeviri özelliğini kullandığınızda, çıkarılan metin şifreli (HTTPS) bir bağlantı üzerinden üçüncü taraf bir çeviri servisine gönderilir. Bu veriyi saklamamız veya günlüğe kaydetmemiz söz konusu değildir.</li>
      </ul>
      <div class="callout">
        Adınızı, e-posta adresinizi, telefon numaranızı, konumunuzu veya diğer kişisel bilgilerinizi toplamıyoruz.
      </div>
    </div>

    <hr>

    <div class="section">
      <div class="section-title">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
        Üçüncü taraf hizmetler
      </div>
      <p>Uygulama yalnızca bir harici hizmet kullanır:</p>
      <ul>
        <li><strong>Çeviri servisi</strong> — Taranan bir belgeden çıkarılan metni çevirdiğinizde, bu metin HTTPS üzerinden harici bir çeviri API'sine iletilir. Bu iletim, özelliğin çalışması için zorunludur. Çeviri sağlayıcısının kendi veri saklama uygulamaları olabilir; lütfen onların gizlilik politikasını inceleyin.</li>
      </ul>
      <p style="margin-top: 0.75rem;">Uygulamada herhangi bir analitik, reklam veya izleme SDK'sı bulunmamaktadır.</p>
    </div>

    <hr>

    <div class="section">
      <div class="section-title">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="11" width="18" height="11" rx="2" ry="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>
        Veri güvenliği
      </div>
      <p>Belgeleriniz ve verileriniz cihazınızda yerel olarak saklanır. Taranan belgelerinize erişimimiz yoktur. Sistem paylaşım sayfası aracılığıyla paylaşılan dosyalar yalnızca açıkça seçtiğiniz uygulamalara aktarılır.</p>
      <p>En güncel işletim sistemi güvenlik korumasından yararlanmak için cihaz yazılımınızı güncel tutmanızı öneririz.</p>
    </div>

    <hr>

    <div class="section">
      <div class="section-title">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg>
        Çocukların gizliliği
      </div>
      <p>Bu uygulama 13 yaşın altındaki çocuklara yönelik değildir. Çocuklardan bilerek kişisel bilgi toplamıyoruz. Bir çocuğun uygulama aracılığıyla kişisel veri sağladığını düşünüyorsanız lütfen bizimle iletişime geçin, gerekli önlemleri alacağız.</p>
    </div>

    <hr>

    <div class="section">
      <div class="section-title">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><polyline points="23 4 23 10 17 10"/><polyline points="1 20 1 14 7 14"/><path d="M3.51 9a9 9 0 0 1 14.85-3.36L23 10M1 14l4.64 4.36A9 9 0 0 0 20.49 15"/></svg>
        Politika değişiklikleri
      </div>
      <p>Bu Gizlilik Politikasını zaman zaman güncelleyebiliriz. Güncelleme yaptığımızda sayfanın üstündeki "Son güncelleme" tarihini değiştireceğiz. Herhangi bir değişikliğin ardından uygulamayı kullanmaya devam etmeniz, güncellenmiş politikayı kabul ettiğiniz anlamına gelir.</p>
    </div>

    <hr>

    <div class="section">
      <div class="section-title">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        İletişim
      </div>
      <p>Bu Gizlilik Politikası hakkında sorularınız için bize ulaşabilirsiniz:</p>
      <div class="contact-row">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        <a href="mailto:support@yourapp.com">support@yourapp.com</a>
      </div>
      <div class="contact-row">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
        <a href="https://yourapp.com/privacy">yourapp.com/privacy</a>
      </div>
    </div>

    <footer>
      <p>Bu gizlilik politikası Scanner: PDF Documents için hazırlanmıştır.<br>
      © 2025 Şirket Adınız. Tüm hakları saklıdır.</p>
    </footer>

  </div>

</div>

<script>
  function setLang(lang, btn) {
    document.querySelectorAll('[lang-content]').forEach(el => el.classList.remove('active'));
    document.querySelector('[lang-content="' + lang + '"]').classList.add('active');
    document.querySelectorAll('.lang-btn').forEach(b => b.classList.remove('active'));
    btn.classList.add('active');
    document.documentElement.lang = lang;
  }
</script>
</body>
</html>
