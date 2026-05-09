'use client';

import Link from 'next/link';
import * as React from 'react';

const sampleAddresses = [
  ['Swiss Ace IBAN reference', 'Office banking identifier', 'iban720109165346779368'],
  ['Swiss Ace public key address', 'ETH / ERC-20 public address', '0x85A93c354ab70a37471847d769aB794b22C5A8bf'],
  ['Swiss Ace BTC public address', 'Bitcoin public address', 'bc1qcyj6qjz7dg9c22ry37km41r4qgl6kr5shyv97f'],
];

const transactions = [
  ['2026-05-03', 'Inbound', 'ETH', '18.2400', '$57,920', 'Counterparty review'],
  ['2026-04-29', 'Outbound', 'USDT', '92,500', '$92,500', 'Stablecoin exposure'],
  ['2026-04-21', 'Inbound', 'BTC', '1.4820', '$103,740', 'Source review'],
  ['2026-04-18', 'Outbound', 'ETH', '7.1800', '$22,810', 'Standard movement'],
];

const variants = {
  intelligence: {
    tone: 'intelligence',
    eyebrow: 'Address intelligence',
    title: 'Public-address value and activity review.',
    intro:
      'A data-led AML page for reviewing a public identifier, indicative balance, recent transaction movement, and supporting evidence in one place.',
    formTitle: 'Submit Address Review',
    formIntro: 'Prepare the public address, client reference, and evidence for Swiss Ace AML review.',
  },
  public: {
    tone: 'public',
    eyebrow: 'Client verification',
    title: 'Verification for public identifiers and client evidence.',
    intro:
      'A polished institutional verification page with a clear public intake path and controlled office review.',
    formTitle: 'Begin Verification',
    formIntro: 'Submit the required public identifier and documents for office review.',
  },
  room: {
    tone: 'room',
    eyebrow: 'Review room',
    title: 'A controlled case room for AML decisioning.',
    intro:
      'A stronger workflow concept with a live case board, evidence queue, review notes, and final intake receipt.',
    formTitle: 'Open Review File',
    formIntro: 'Complete the case file and submit it for Swiss Ace review.',
  },
};

function buildReviewReference(identifier) {
  const clean = identifier.replace(/[^a-z0-9]/gi, '').toUpperCase();
  return `SA-KYC-${clean ? clean.slice(-6) : 'DRAFT'}`;
}

function copyFallback(text) {
  const area = document.createElement('textarea');
  area.value = text;
  area.setAttribute('readonly', '');
  area.style.position = 'fixed';
  area.style.opacity = '0';
  document.body.appendChild(area);
  area.select();
  document.execCommand('copy');
  document.body.removeChild(area);
}

function Header({ variant }) {
  return (
    <header className="sx-topbar">
      <Link className="sx-brand" href="/">
        <img src="/brand/swiss-ace-mark.svg" alt="" aria-hidden="true" />
        <span>Swiss Ace</span>
        <small>{variant.eyebrow}</small>
      </Link>
      <nav aria-label="Verification navigation">
        <Link href="/">Home</Link>
        <Link href="/capabilities/regulatory-compliance/">Compliance</Link>
        <Link href="/security/">Security</Link>
        <Link href="/contact/">Contact</Link>
      </nav>
    </header>
  );
}

function UploadBox({ addFiles, dragging, files, inputId, removeFile, setDragging }) {
  return (
    <section className="sx-card sx-upload">
      <div className="sx-card-head">
        <span>Evidence</span>
        <strong>Document intake</strong>
      </div>
      <label
        className={`sx-drop ${dragging ? 'is-dragging' : ''}`}
        htmlFor={inputId}
        onDragEnter={(event) => {
          event.preventDefault();
          setDragging(true);
        }}
        onDragOver={(event) => event.preventDefault()}
        onDragLeave={() => setDragging(false)}
        onDrop={(event) => {
          event.preventDefault();
          setDragging(false);
          addFiles(event.dataTransfer.files);
        }}
      >
        <input
          accept=".pdf,.png,.jpg,.jpeg,.heic,image/png,image/jpeg,application/pdf"
          id={inputId}
          multiple
          onChange={(event) => addFiles(event.target.files)}
          type="file"
        />
        <span>PDF / JPG / PNG / HEIC</span>
        <strong>Click or drag files to upload</strong>
        <small>Maximum 10MB per file</small>
      </label>
      <div className="sx-files" aria-live="polite">
        {files.length ? (
          files.map((file) => (
            <div key={file.id}>
              <span>{file.name}</span>
              <small>{Math.max(1, Math.round(file.size / 1024))} KB</small>
              <button onClick={() => removeFile(file.id)} type="button" aria-label={`Remove ${file.name}`}>
                Remove
              </button>
            </div>
          ))
        ) : (
          <p>No documents added yet.</p>
        )}
      </div>
    </section>
  );
}

function AddressExamples({ copied, copyAddress }) {
  return (
    <section className="sx-card sx-examples">
      <div className="sx-card-head">
        <span>Swiss Ace address</span>
        <strong>Public key address</strong>
      </div>
      {sampleAddresses.map(([label, network, value]) => (
        <article key={label}>
          <div>
            <span>{label}</span>
            <small>{network}</small>
            <code>{value}</code>
          </div>
          <button onClick={() => copyAddress(value, label)} type="button">
            Copy
          </button>
        </article>
      ))}
      <p>{copied ? `${copied} copied.` : 'Use only the public key/address confirmed by the Swiss Ace office. These records are for verification intake, not transfer instructions.'}</p>
    </section>
  );
}

function Receipt({ files, reviewReference }) {
  return (
    <div className="sx-receipt" aria-live="polite">
      <span>Review prepared</span>
      <strong>{reviewReference}</strong>
      <dl>
        <div>
          <dt>AML check</dt>
          <dd>Queued for review</dd>
        </div>
        <div>
          <dt>Documents</dt>
          <dd>{files.length ? `${files.length} attached` : 'None attached'}</dd>
        </div>
        <div>
          <dt>Decision</dt>
          <dd>Office issued separately</dd>
        </div>
      </dl>
    </div>
  );
}

function VerificationForm({
  canSubmit,
  cleanIdentifier,
  files,
  form,
  pasteIdentifier,
  resetReview,
  reviewReference,
  submitReview,
  submitted,
  updateField,
  variant,
}) {
  return (
    <form className="sx-form sx-card" onSubmit={submitReview}>
      <div className="sx-form-title">
        <span>{variant.eyebrow}</span>
        <h2>{variant.formTitle}</h2>
        <p>{variant.formIntro}</p>
      </div>
      <div className="sx-form-grid">
        <label>
          <span>Name</span>
          <input
            autoComplete="name"
            onChange={updateField('fullName')}
            placeholder="Your full name"
            value={form.fullName}
          />
        </label>
        <label>
          <span>Reference no.</span>
          <input
            autoComplete="off"
            onChange={updateField('reference')}
            placeholder={buildReviewReference(cleanIdentifier)}
            value={form.reference}
          />
        </label>
      </div>
      <label className="sx-wide">
        <span>Crypto address, transaction reference, or IBAN</span>
        <div>
          <input
            autoComplete="off"
            onChange={updateField('identifier')}
            placeholder="Paste public identifier here"
            spellCheck="false"
            value={form.identifier}
          />
          <button onClick={pasteIdentifier} type="button">
            Paste
          </button>
        </div>
      </label>
      <label className="sx-wide">
        <span>Office note</span>
        <textarea
          onChange={updateField('note')}
          placeholder="Optional note for the Swiss Ace review team"
          rows={4}
          value={form.note}
        />
      </label>
      <p className="sx-safe">
        Public identifiers and evidence only. Never submit passwords, seed phrases, private keys,
        wallet approvals, or transfer instructions.
      </p>
      <div className="sx-actions">
        <button className="sx-submit" disabled={!canSubmit} type="submit">
          Submit verification
        </button>
        <button className="sx-secondary" onClick={resetReview} type="button">
          Send new verification
        </button>
      </div>
      {submitted ? <Receipt files={files} reviewReference={reviewReference} /> : null}
    </form>
  );
}

function CaseStats({ cleanIdentifier, files, reviewReference, submitted }) {
  return (
    <section className="sx-stats">
      {[
        ['Review reference', reviewReference],
        ['Identifier', cleanIdentifier ? 'Received' : 'Awaiting input'],
        ['Evidence', files.length ? `${files.length} files` : 'No files'],
        ['AML status', submitted ? 'Prepared' : 'Draft'],
      ].map(([label, value]) => (
        <article key={label}>
          <span>{label}</span>
          <strong>{value}</strong>
        </article>
      ))}
    </section>
  );
}

function IntelligencePage(props) {
  const { cleanIdentifier, files, reviewReference, submitted, variant } = props;
  return (
    <>
      <section className="sx-intel-hero">
        <div>
          <p>{variant.eyebrow}</p>
          <h1>{variant.title}</h1>
          <span>{variant.intro}</span>
        </div>
        <div className="sx-value-card">
          <span>Indicative address value</span>
          <strong>$428,940</strong>
          <p>Across BTC, ETH, and stablecoin activity prepared for office review.</p>
        </div>
      </section>
      <CaseStats
        cleanIdentifier={cleanIdentifier}
        files={files}
        reviewReference={reviewReference}
        submitted={submitted}
      />
      <section className="sx-intel-grid">
        <div className="sx-intel-main">
          <section className="sx-card sx-ledger">
            <div className="sx-card-head">
              <span>Activity</span>
              <strong>Recent public transactions</strong>
            </div>
            <div className="sx-ledger-table">
              {transactions.map(([date, direction, asset, amount, value, note]) => (
                <article key={`${date}-${asset}-${amount}`}>
                  <span>{date}</span>
                  <strong>{direction}</strong>
                  <code>{amount} {asset}</code>
                  <b>{value}</b>
                  <small>{note}</small>
                </article>
              ))}
            </div>
          </section>
          <VerificationForm {...props} />
        </div>
        <aside className="sx-intel-side">
          <AddressExamples {...props} />
          <UploadBox {...props} inputId="sx-intelligence-files" />
        </aside>
      </section>
    </>
  );
}

function PublicPage(props) {
  const { cleanIdentifier, files, reviewReference, submitted, variant } = props;
  return (
    <>
      <section className="sx-public-hero">
        <img src="/images/capabilities-singapore-financial-district-real.jpg" alt="Singapore financial district" />
        <div>
          <p>{variant.eyebrow}</p>
          <h1>{variant.title}</h1>
          <span>{variant.intro}</span>
        </div>
      </section>
      <CaseStats
        cleanIdentifier={cleanIdentifier}
        files={files}
        reviewReference={reviewReference}
        submitted={submitted}
      />
      <section className="sx-public-layout">
        <div>
          <section className="sx-public-copy sx-card">
            <span>Review scope</span>
            <h2>Public identifier, evidence, and AML context.</h2>
            <p>
              Swiss Ace prepares submitted identifiers for internal review. The page does not request
              private wallet material and does not issue transfer instructions.
            </p>
          </section>
          <UploadBox {...props} inputId="sx-public-files" />
        </div>
        <VerificationForm {...props} />
        <AddressExamples {...props} />
      </section>
    </>
  );
}

function RoomPage(props) {
  const { cleanIdentifier, files, reviewReference, submitted, variant } = props;
  const lanes = [
    ['Intake', cleanIdentifier ? 'Identifier received' : 'Awaiting identifier'],
    ['Evidence', files.length ? `${files.length} files attached` : 'Awaiting documents'],
    ['AML', submitted ? 'Review file prepared' : 'Pending submission'],
  ];

  return (
    <>
      <section className="sx-room-shell">
        <aside className="sx-room-side">
          <p>{variant.eyebrow}</p>
          <h1>{variant.title}</h1>
          <span>{variant.intro}</span>
          <div className="sx-room-ref">
            <small>Review reference</small>
            <strong>{reviewReference}</strong>
          </div>
        </aside>
        <div className="sx-room-main">
          <section className="sx-room-board">
            {lanes.map(([title, text]) => (
              <article key={title}>
                <span>{title}</span>
                <strong>{text}</strong>
                <p>Office decision issued separately after review.</p>
              </article>
            ))}
          </section>
          <div className="sx-room-grid">
            <VerificationForm {...props} />
            <div className="sx-room-stack">
              <UploadBox {...props} inputId="sx-room-files" />
              <AddressExamples {...props} />
            </div>
          </div>
        </div>
      </section>
    </>
  );
}

export default function SwissAceKycExperimentalPage({ design = 'intelligence' }) {
  const variant = variants[design] || variants.intelligence;
  const [form, setForm] = React.useState({
    fullName: '',
    reference: '',
    identifier: '',
    note: '',
  });
  const [files, setFiles] = React.useState([]);
  const [copied, setCopied] = React.useState('');
  const [dragging, setDragging] = React.useState(false);
  const [submitted, setSubmitted] = React.useState(false);

  const cleanIdentifier = form.identifier.trim();
  const reviewReference = form.reference.trim() || buildReviewReference(cleanIdentifier);
  const canSubmit = form.fullName.trim().length > 1 && cleanIdentifier.length > 5;

  function updateField(field) {
    return (event) => {
      setSubmitted(false);
      setForm((current) => ({ ...current, [field]: event.target.value }));
    };
  }

  function addFiles(fileList) {
    const incoming = Array.from(fileList || []);
    const nextFiles = incoming
      .filter((file) => file.size <= 10 * 1024 * 1024)
      .map((file) => ({
        id: `${file.name}-${file.size}-${file.lastModified}`,
        name: file.name,
        size: file.size,
      }));

    if (!nextFiles.length) return;
    setSubmitted(false);
    setFiles((current) => {
      const known = new Set(current.map((item) => item.id));
      return [...current, ...nextFiles.filter((item) => !known.has(item.id))].slice(0, 6);
    });
  }

  async function copyAddress(value, label) {
    try {
      if (navigator.clipboard?.writeText) {
        await navigator.clipboard.writeText(value);
      } else {
        copyFallback(value);
      }
      setCopied(label);
      window.setTimeout(() => setCopied(''), 1600);
    } catch {
      setCopied('Copy unavailable');
      window.setTimeout(() => setCopied(''), 1600);
    }
  }

  async function pasteIdentifier() {
    try {
      const text = await navigator.clipboard.readText();
      setForm((current) => ({ ...current, identifier: text }));
      setSubmitted(false);
    } catch {
      setCopied('Paste unavailable');
      window.setTimeout(() => setCopied(''), 1600);
    }
  }

  function removeFile(id) {
    setFiles((current) => current.filter((file) => file.id !== id));
    setSubmitted(false);
  }

  function submitReview(event) {
    event.preventDefault();
    if (!canSubmit) return;
    setSubmitted(true);
  }

  function resetReview() {
    setForm({ fullName: '', reference: '', identifier: '', note: '' });
    setFiles([]);
    setCopied('');
    setDragging(false);
    setSubmitted(false);
  }

  const props = {
    addFiles,
    canSubmit,
    cleanIdentifier,
    copied,
    copyAddress,
    dragging,
    files,
    form,
    pasteIdentifier,
    removeFile,
    resetReview,
    reviewReference,
    setDragging,
    submitReview,
    submitted,
    updateField,
    variant,
  };

  return (
    <main className={`sx-page sx-tone-${variant.tone}`}>
      <Header variant={variant} />
      {variant.tone === 'intelligence' ? <IntelligencePage {...props} /> : null}
      {variant.tone === 'public' ? <PublicPage {...props} /> : null}
      {variant.tone === 'room' ? <RoomPage {...props} /> : null}

      <style jsx global>{`
        .sx-page {
          --ink: #111923;
          --muted: #5e6a73;
          --paper: #ffffff;
          --soft: #f4f7f6;
          --line: #d7e0e3;
          --accent: #1f7288;
          --green: #247a5c;
          background: var(--soft);
          color: var(--ink);
          font-family: 'DM Sans', Arial, sans-serif;
          min-height: 100vh;
        }

        .sx-page a {
          color: inherit;
          text-decoration: none;
        }

        .sx-page button,
        .sx-page input,
        .sx-page textarea {
          font: inherit;
        }

        .sx-topbar {
          align-items: center;
          background: rgba(255, 255, 255, .94);
          border-bottom: 1px solid var(--line);
          display: flex;
          gap: 32px;
          justify-content: space-between;
          min-height: 78px;
          padding: 0 clamp(18px, 5vw, 70px);
          position: sticky;
          top: 0;
          z-index: 20;
          backdrop-filter: blur(14px);
        }

        .sx-brand {
          align-items: center;
          display: grid;
          grid-template-columns: 30px auto;
          column-gap: 12px;
          line-height: 1;
        }

        .sx-brand img {
          height: 30px;
          width: 30px;
        }

        .sx-brand span {
          font-family: 'Cormorant Garamond', Georgia, serif;
          font-size: 22px;
          font-weight: 600;
          letter-spacing: .08em;
          text-transform: uppercase;
        }

        .sx-brand small,
        .sx-topbar nav a,
        .sx-intel-hero p,
        .sx-public-hero p,
        .sx-room-side p,
        .sx-card-head span,
        .sx-form-title span,
        .sx-public-copy span,
        .sx-room-board span,
        .sx-stats span,
        .sx-examples article span {
          color: var(--accent);
          font-size: 10px;
          font-weight: 900;
          letter-spacing: .22em;
          text-transform: uppercase;
        }

        .sx-brand small {
          grid-column: 2;
          margin-top: 5px;
        }

        .sx-topbar nav {
          display: flex;
          gap: clamp(16px, 3vw, 42px);
        }

        .sx-intel-hero,
        .sx-public-layout,
        .sx-intel-grid,
        .sx-room-grid {
          display: grid;
          gap: 18px;
        }

        .sx-intel-hero {
          grid-template-columns: minmax(0, 1fr) minmax(320px, .36fr);
          padding: clamp(50px, 7vw, 96px) clamp(18px, 6vw, 88px) 24px;
        }

        .sx-intel-hero h1,
        .sx-public-hero h1,
        .sx-room-side h1,
        .sx-form-title h2,
        .sx-card-head strong,
        .sx-public-copy h2,
        .sx-value-card strong {
          font-family: 'Cormorant Garamond', Georgia, serif;
          font-weight: 500;
          letter-spacing: 0;
        }

        .sx-intel-hero h1,
        .sx-public-hero h1,
        .sx-room-side h1 {
          font-size: clamp(54px, 7vw, 108px);
          line-height: .9;
          margin: 14px 0 22px;
          max-width: 920px;
        }

        .sx-intel-hero span,
        .sx-public-hero span,
        .sx-room-side > span,
        .sx-form-title p,
        .sx-public-copy p,
        .sx-value-card p {
          color: var(--muted);
          display: block;
          font-size: 15px;
          line-height: 1.8;
          max-width: 720px;
        }

        .sx-value-card,
        .sx-card,
        .sx-stats article,
        .sx-room-board article {
          background: var(--paper);
          border: 1px solid var(--line);
        }

        .sx-value-card {
          align-content: center;
          display: grid;
          padding: clamp(24px, 4vw, 42px);
        }

        .sx-value-card span {
          color: var(--accent);
          font-size: 10px;
          font-weight: 900;
          letter-spacing: .22em;
          text-transform: uppercase;
        }

        .sx-value-card strong {
          color: var(--green);
          display: block;
          font-size: clamp(48px, 5vw, 74px);
          line-height: 1;
          margin: 14px 0;
        }

        .sx-stats {
          display: grid;
          grid-template-columns: repeat(4, minmax(0, 1fr));
          margin: 0 clamp(18px, 6vw, 88px) 18px;
        }

        .sx-stats article {
          border-right: 0;
          min-width: 0;
          padding: 20px;
        }

        .sx-stats article:last-child {
          border-right: 1px solid var(--line);
        }

        .sx-stats strong {
          display: block;
          font-family: 'Courier New', monospace;
          font-size: 14px;
          margin-top: 10px;
          overflow-wrap: anywhere;
        }

        .sx-intel-grid {
          grid-template-columns: minmax(0, 1fr) minmax(320px, .42fr);
          padding: 0 clamp(18px, 6vw, 88px) clamp(44px, 6vw, 88px);
        }

        .sx-intel-main,
        .sx-intel-side,
        .sx-room-stack {
          display: grid;
          gap: 18px;
          align-content: start;
        }

        .sx-card {
          padding: clamp(22px, 3vw, 36px);
        }

        .sx-card-head {
          margin-bottom: 20px;
        }

        .sx-card-head strong {
          display: block;
          font-size: clamp(28px, 3vw, 42px);
          line-height: 1;
          margin-top: 8px;
        }

        .sx-ledger-table {
          display: grid;
          gap: 0;
        }

        .sx-ledger-table article {
          align-items: center;
          border-top: 1px solid var(--line);
          display: grid;
          gap: 14px;
          grid-template-columns: 110px 110px 1fr 120px 1.2fr;
          min-height: 58px;
          padding: 12px 0;
        }

        .sx-ledger-table span,
        .sx-ledger-table small,
        .sx-files small,
        .sx-drop small,
        .sx-examples small,
        .sx-examples > p {
          color: var(--muted);
          font-size: 12px;
          line-height: 1.55;
        }

        .sx-ledger-table strong {
          font-size: 13px;
          text-transform: uppercase;
        }

        .sx-ledger-table code,
        .sx-examples code {
          font-family: 'Courier New', monospace;
          overflow-wrap: anywhere;
        }

        .sx-ledger-table b {
          color: var(--green);
          font-size: 13px;
        }

        .sx-form {
          display: grid;
          gap: 22px;
        }

        .sx-form-title h2 {
          font-size: clamp(36px, 4vw, 60px);
          line-height: 1;
          margin: 8px 0 12px;
        }

        .sx-form-grid {
          display: grid;
          gap: 20px;
          grid-template-columns: 1fr 1fr;
        }

        .sx-form label {
          display: grid;
          gap: 9px;
        }

        .sx-form label > span {
          color: var(--accent);
          font-size: 10px;
          font-weight: 900;
          letter-spacing: .18em;
          text-transform: uppercase;
        }

        .sx-form input,
        .sx-form textarea {
          background: transparent;
          border: 0;
          border-bottom: 1px solid var(--line);
          color: var(--ink);
          min-height: 44px;
          outline: 0;
          padding: 9px 0 13px;
          width: 100%;
        }

        .sx-form textarea {
          border: 1px solid var(--line);
          min-height: 112px;
          padding: 14px;
          resize: vertical;
        }

        .sx-wide > div {
          align-items: center;
          display: grid;
          gap: 12px;
          grid-template-columns: minmax(0, 1fr) auto;
        }

        .sx-page button {
          cursor: pointer;
        }

        .sx-wide button,
        .sx-examples button,
        .sx-files button {
          background: transparent;
          border: 1px solid var(--ink);
          color: var(--ink);
          font-size: 10px;
          font-weight: 900;
          letter-spacing: .18em;
          min-height: 34px;
          padding: 8px 12px;
          text-transform: uppercase;
        }

        .sx-safe {
          border-left: 1px solid var(--accent);
          color: var(--muted);
          font-size: 12px;
          line-height: 1.65;
          margin: 0;
          padding-left: 16px;
        }

        .sx-actions {
          display: flex;
          flex-wrap: wrap;
          gap: 12px;
        }

        .sx-submit,
        .sx-secondary {
          border: 1px solid var(--ink);
          font-size: 11px;
          font-weight: 900;
          letter-spacing: .2em;
          min-height: 50px;
          padding: 14px 18px;
          text-transform: uppercase;
        }

        .sx-submit {
          background: var(--ink);
          color: var(--paper);
          min-width: 212px;
        }

        .sx-submit:disabled {
          cursor: not-allowed;
          opacity: .42;
        }

        .sx-secondary {
          background: transparent;
          color: var(--ink);
          min-width: 230px;
        }

        .sx-drop {
          align-items: center;
          border: 1px dashed var(--accent);
          cursor: pointer;
          display: grid;
          justify-items: center;
          min-height: 176px;
          padding: 26px;
          text-align: center;
        }

        .sx-drop.is-dragging {
          background: rgba(31, 114, 136, .08);
        }

        .sx-drop input {
          display: none;
        }

        .sx-drop span {
          color: var(--accent);
          font-size: 10px;
          font-weight: 900;
          letter-spacing: .22em;
          text-transform: uppercase;
        }

        .sx-drop strong {
          display: block;
          font-family: 'Cormorant Garamond', Georgia, serif;
          font-size: 28px;
          font-weight: 500;
          margin-top: 14px;
        }

        .sx-files {
          display: grid;
          gap: 8px;
          margin-top: 16px;
        }

        .sx-files p {
          color: var(--muted);
          font-size: 13px;
          margin: 0;
        }

        .sx-files div {
          align-items: center;
          border: 1px solid var(--line);
          display: grid;
          gap: 10px;
          grid-template-columns: minmax(0, 1fr) auto auto;
          min-height: 44px;
          padding: 8px 10px;
        }

        .sx-files span {
          font-size: 13px;
          overflow-wrap: anywhere;
        }

        .sx-examples article {
          align-items: center;
          border-top: 1px solid var(--line);
          display: grid;
          gap: 16px;
          grid-template-columns: minmax(0, 1fr) auto;
          min-height: 84px;
          padding: 14px 0;
        }

        .sx-examples article span,
        .sx-examples article small {
          display: block;
        }

        .sx-examples article small {
          margin-top: 4px;
        }

        .sx-examples code {
          display: block;
          font-size: 12px;
          margin-top: 10px;
        }

        .sx-examples > p {
          border-top: 1px solid var(--line);
          margin: 0;
          padding-top: 14px;
        }

        .sx-receipt {
          background: rgba(36, 122, 92, .08);
          border: 1px solid rgba(36, 122, 92, .26);
          padding: 18px;
        }

        .sx-receipt > span {
          color: var(--green);
          font-size: 10px;
          font-weight: 900;
          letter-spacing: .2em;
          text-transform: uppercase;
        }

        .sx-receipt > strong {
          color: var(--green);
          display: block;
          font-family: 'Cormorant Garamond', Georgia, serif;
          font-size: 34px;
          line-height: 1;
          margin-top: 10px;
        }

        .sx-receipt dl {
          display: grid;
          gap: 8px;
          grid-template-columns: repeat(3, minmax(0, 1fr));
          margin: 16px 0 0;
        }

        .sx-receipt div {
          background: rgba(255, 255, 255, .58);
          border: 1px solid rgba(36, 122, 92, .18);
          padding: 12px;
        }

        .sx-receipt dt {
          color: var(--muted);
          font-size: 9px;
          font-weight: 900;
          letter-spacing: .18em;
          text-transform: uppercase;
        }

        .sx-receipt dd {
          font-size: 13px;
          font-weight: 800;
          margin: 7px 0 0;
        }

        .sx-tone-public {
          --accent: #315d71;
          --soft: #f7f6f2;
        }

        .sx-public-hero {
          display: grid;
          min-height: 620px;
          position: relative;
        }

        .sx-public-hero img {
          display: block;
          filter: grayscale(.12) saturate(.82) contrast(1.04);
          height: 100%;
          inset: 0;
          object-fit: cover;
          position: absolute;
          width: 100%;
        }

        .sx-public-hero::after {
          background: linear-gradient(90deg, rgba(247, 246, 242, .97), rgba(247, 246, 242, .72), rgba(247, 246, 242, .12));
          content: '';
          inset: 0;
          position: absolute;
        }

        .sx-public-hero div {
          align-self: center;
          padding: clamp(54px, 8vw, 110px) clamp(18px, 6vw, 92px);
          position: relative;
          z-index: 1;
        }

        .sx-public-layout {
          grid-template-columns: minmax(280px, .78fr) minmax(420px, 1fr) minmax(300px, .78fr);
          padding: 0 clamp(18px, 6vw, 88px) clamp(44px, 6vw, 88px);
        }

        .sx-public-layout > div {
          display: grid;
          gap: 18px;
          align-content: start;
        }

        .sx-public-copy h2 {
          font-size: clamp(34px, 4vw, 58px);
          line-height: 1;
          margin: 10px 0 16px;
        }

        .sx-tone-room {
          --accent: #6db69a;
          --soft: #0e2f31;
          --line: rgba(255, 255, 255, .16);
          --paper: #f8faf7;
          background: #0e2f31;
        }

        .sx-room-shell {
          background: #0e2f31;
          display: grid;
          grid-template-columns: minmax(430px, .46fr) minmax(0, 1fr);
          min-height: calc(100vh - 78px);
        }

        .sx-room-side {
          color: #fff;
          display: grid;
          gap: 26px;
          align-content: start;
          padding: clamp(34px, 5vw, 72px);
        }

        .sx-room-side h1 {
          color: #fff;
          font-size: clamp(44px, 4.5vw, 72px);
          line-height: .96;
          max-width: 360px;
        }

        .sx-room-side > span {
          color: rgba(255, 255, 255, .76);
        }

        .sx-room-ref {
          border: 1px solid rgba(255, 255, 255, .22);
          padding: 22px;
        }

        .sx-room-ref small {
          color: rgba(255, 255, 255, .62);
          display: block;
          font-size: 10px;
          font-weight: 900;
          letter-spacing: .2em;
          text-transform: uppercase;
        }

        .sx-room-ref strong {
          display: block;
          font-family: 'Courier New', monospace;
          margin-top: 12px;
          overflow-wrap: anywhere;
        }

        .sx-room-main {
          background: #f4f7f6;
          display: grid;
          gap: 18px;
          padding: clamp(18px, 3vw, 38px);
        }

        .sx-room-board {
          display: grid;
          gap: 18px;
          grid-template-columns: repeat(3, minmax(0, 1fr));
        }

        .sx-room-board article {
          padding: 22px;
        }

        .sx-room-board strong {
          display: block;
          font-family: 'Cormorant Garamond', Georgia, serif;
          font-size: 30px;
          line-height: 1;
          margin-top: 12px;
        }

        .sx-room-board p {
          color: var(--muted);
          font-size: 13px;
          line-height: 1.6;
        }

        .sx-room-grid {
          grid-template-columns: minmax(0, 1fr) minmax(320px, .48fr);
        }

        @media (max-width: 1120px) {
          .sx-intel-hero,
          .sx-intel-grid,
          .sx-public-layout,
          .sx-room-shell,
          .sx-room-grid {
            grid-template-columns: 1fr;
          }

          .sx-room-board,
          .sx-stats {
            grid-template-columns: 1fr 1fr;
          }
        }

        @media (max-width: 700px) {
          .sx-topbar {
            align-items: start;
            flex-direction: column;
            gap: 16px;
            padding-bottom: 16px;
            padding-top: 16px;
            position: relative;
          }

          .sx-topbar nav {
            flex-wrap: wrap;
          }

          .sx-intel-hero,
          .sx-intel-grid,
          .sx-public-layout,
          .sx-room-main,
          .sx-room-side {
            padding-left: 14px;
            padding-right: 14px;
          }

          .sx-intel-hero h1,
          .sx-public-hero h1,
          .sx-room-side h1 {
            font-size: 50px;
          }

          .sx-public-hero {
            min-height: 560px;
          }

          .sx-form-grid,
          .sx-wide > div,
          .sx-files div,
          .sx-examples article,
          .sx-receipt dl,
          .sx-room-board,
          .sx-stats,
          .sx-ledger-table article {
            grid-template-columns: 1fr;
          }

          .sx-stats {
            margin-left: 14px;
            margin-right: 14px;
          }

          .sx-actions {
            display: grid;
          }

          .sx-submit,
          .sx-secondary {
            width: 100%;
          }

          .sx-card {
            padding: 20px;
          }

          .sx-examples code,
          .sx-ledger-table code {
            font-size: 11px;
          }
        }
      `}</style>
    </main>
  );
}
