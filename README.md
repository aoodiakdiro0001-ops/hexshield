# 🛡️ HexShield — Niche Security Tools (MIT)

Free defensive security tools for site owners & developers.
**100% client-side** — no data ever leaves the browser.

## Tools

1. **🔒 Security Headers Check** — grades HTTP security headers
   (HSTS, CSP, X-Frame-Options, X-Content-Type-Options, Referrer-Policy,
   Permissions-Policy, COOP/COEP/CORP, leak headers). Auto mode reads
   visible headers via a public CORS proxy; **manual mode** (paste cURL
   output) is fully accurate. `Set-Cookie` flags can never be read by JS —
   the tool says so openly.
2. **📜 Smart Contract Auditor (Solidity)** — 11 static patterns
   (floating pragma, pre-0.8 without SafeMath, tx.origin, reentrancy,
   unchecked calls, delegatecall, selfdestruct, timestamp, unprotected
   mint, ecrecover, old-style constructor) with line numbers, severity,
   explanations and fixes. Markdown report download included.

## Run

```bash
cd hexshield
python3 -m http.server 8080
# → http://localhost:8080
```

## Money / Para kazanma

- **Ads:** `CONFIG.ads` içine AdSense (`client`+`slot`) veya Carbon
  (`carbonServe`+`carbonPlacement`) ID'lerini yazın; ID yoksa şık
  "Advertise here" kutusu görünür. Dev/tech trafiği = yüksek CPC.
- **Pro Reports:** Headers Pro **$5**, Contract Pro **$9** (tek ödeme).
  Ödeme BTC (+USDT adresleri eklenebilir) → TXID ile kilit açma →
  yazdırılabilir detay rapor. BTC karşılığı CoinGecko canlı kuruyla gösterilir.
- **Owner:** footer'daki Owner bağlantısı + şifre ile satış listesi
  (`hs_orders`). Gerçek parayla satıştan önce BTCPay/xPub doğrulamalı
  backend şart — mevcut kilit demo düzeyindedir.

## Honest limits

- Header auto-scan sees only proxy-visible headers; use manual paste for audits.
- Contract scan is pattern-based pre-screening, **not** a professional audit.
  Mainnet → OpenZeppelin / Trail of Bits / ConsenSys Diligence.

## License

MIT.

## Telegram (@BaranScanBot)

- Footer'da herkese açık "Telegram" butonu (`t.me/BaranScanBot`) — ziyaretçi
  doğrudan bota yazar, ek ayar gerekmez.
- Sipariş/satış bildirimleri (`tgSend`) yalnızca `CONFIG`... `TG.chat`
  doluysa sahibine gider. Chat ID'yi @userinfobot'tan alıp `TG.chat`e yazın.
- ⚠️ **GÜVENLİK:** Bot tokeni herkese açık istemci kodundadır; kaynağı
  gören herkes bot adına mesaj gönderebilir. Kötüye kullanımda BotFather'dan
  tokeni yenileyin ve asla bu botla hassas işlem yapmayın. Gerçek çözüm:
  backend proxy.
