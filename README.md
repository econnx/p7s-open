# P7S Open

**Open a signed `.p7s` file in your browser.** Get the original PDF / DOCX back and see who signed it and when.

→ **https://econnx.github.io/p7s-open/**

Signed documents (Ukrainian КЕП from Diia / id.gov.ua, EU qualified signatures, S/MIME, etc.) often arrive as `document.docx.p7s`. macOS and Windows can't open them — on a Mac double-clicking one even launches Keychain Access. The document is still inside, untouched: a `.p7s` is a CMS / PKCS#7 container with the file plus the signatures.

P7S Open:

- extracts the embedded document (PDF, DOCX, XLSX, images…) and lets you download it with the right name;
- shows the signer certificates (name, issuer, validity) and the signing time;
- handles nested signatures, BER indefinite lengths, base64/PEM input;
- tells you when the signature is *detached* (the .p7s holds only the signature).

Everything runs locally in your browser. Nothing is uploaded. One HTML file, no dependencies, ~200 lines including a tiny ASN.1 parser.

It does **not** verify that the signature is cryptographically valid — that needs the certificate authorities' trust lists. Use your government's verification service for an official check.

## Run locally

Just open `index.html`.

## License

MIT
