# 양도체 표피깊이 계산기

양도체 근사에서 전자기장 진폭의 1/e 감쇠 깊이 계산

- Plan ID: E085
- App: https://nanalab.kr/eng-skin-depth/
- Repository: https://github.com/NaNaCompany/eng-skin-depth
- Formula: `δ = √(1/(πf μ₀μ_r σ))`
- Output: 표피깊이 δ

## Model

f,μ_r,σ>0. 주파수에 맞는 선형 물성과 양도체 근사를 사용한다. 깊이는 진폭의 1/e 기준이다. 변위전류·강자성 비선형·유한 두께·표면 거칠기는 제외한다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `0.00208980678507685`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
