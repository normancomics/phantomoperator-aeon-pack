# PhantomOperator Aeon Skill Pack

Aeon community pack for using [PhantomOperator](https://freysaai.freysa.dev), an authorized privacy and public-exposure analysis API.

Install after the pack is listed:

```bash
bin/install-skill-pack normancomics/phantomoperator-aeon-pack
```

The skill is disabled by default. Paid calls use USDC on Base via x402 with an operator-provided `AEON_X402_WALLET_PRIVATE_KEY`; the skill enforces a hard $0.50 per-call and per-run cap. PhantomOperator is externally operated and receives paid settlements at `0xC5f20C3Ad7B730B34620ecF39c2C5681482A6Cd6`. Read `skills/phantomoperator/SKILL.md` for authorization, trust-boundary, and wallet requirements.
