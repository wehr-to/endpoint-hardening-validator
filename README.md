# 🔐 Endpoint Hardening Validator (API or CLI)

## 🎯 Purpose
Scan any HTTPS endpoint or small web app for hardening misconfigurations:
- Security headers
- Dangerous HTTP methods
- Weak TLS posture
- Cookie settings
- CORS laxness

## 🔧 Tech Stack
- FastAPI for API interface
- Optional: HTML report output

## 🔎 Checks
- **Headers**: CSP, HSTS, X-Content-Type-Options, Referrer-Policy
- **HTTP Verbs**: Blocks TRACE, PUT, OPTIONS
- **TLS**: Version check, cipher strength
- **Cookies**: Secure, HttpOnly, SameSite flags
- **CORS**: Wildcards or insecure origin setups

## 🔐 Security Value
- OWASP A05 (Security Misconfiguration)
- OWASP A08 (Software/Data Integrity Failures)
- OWASP A09 (Logging & Monitoring Failures)
- Great for internal hardening reviews or CI checks

## 🚀 Getting Started
```bash
# Clone repo
$ git clone https://github.com/yourusername/endpoint-hardening-validator.git
$ cd endpoint-hardening-validator

# Run CLI
$ python run_cli.py --target https://example.com

# Or run API
$ uvicorn run_api:app --reload
```

## 🔄 Bonus Feature
- Create a `repo.json` with target metadata (e.g., GitHub Pages, staging URLs) to automate scans in test environments.

## ✅ To Do
- [ ] Add HTML report generator
- [ ] Add automated TLS scan via `ssl` or `requests` hooks
- [ ] Visualize score by category (headers, TLS, CORS)
- [ ] Add rate limit to prevent abuse via API

## 📄 License
MIT
