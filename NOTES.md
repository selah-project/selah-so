# Qoraalada Tarjumaadda — Translation Notes

*Faylkan wuxuu muujinayaa aayad kasta oo gacan dad ama go'aan taabtay
tarjumaadda Soomaaliga. Qoraalada kale waa Ingiriisi — waxay ka hadlaan
qaab-dhismeedka Cibraaniga iyo tixraacyada.*

This file records every verse where a human hand or a ruling touched the
Somali rendering — the fiftieth chair, **the jubilee** (Leviticus 25:10) — so
any verse can be audited: machine-pressed under the rails, hand-rendered, or
ruled, and why. Rails: the Selah Somali discipline (Yahweh / Elohim at the
Name seat; ⟨את⟩ total; ⟨…⟩ marks supplied words only; Sheool never *Naar* /
*Jahannamo*; Masiix never *Kiristoos*; Rabbi(ga) / Eebbe / Ilaah(ay) at the
Name seat and Yehowah / Jehofa rejected).

## The burn and the gleaning (2026-08-31 → 2026-09-01)

The altar-fire relay rendered the corpus overnight (lit 20:40, complete
04:08) and finished with **219 residue** verses, pressed one per call. The
census flagged content faults and every flagged verse was deleted and
re-rendered through the rails, round by round: **1,054 → 152 → 42 → 11**. The
eleven that survived three renders were repaired by hand (below). Final
census: Yahweh 5,797 · Elohim 1,804 · ⟨את⟩ in 7,842 verses · every leak
class zero.

## Two false-positive classes found in the tooling — exposed

- **`naar` is fire.** The cloned census flagged *naar* as the rejected
  Sheol-word. In Somali *naar* renders אש (fire) lawfully in 28 verses
  (1 Kgs 18:23–25, Gen 19:24, Ezek 5:4 …). The rule was narrowed to the
  שאול seat only (`dev/scripts/so_census.clj`, `so_gleaning.clj`). Final
  count at the Sheol seat: 0.
- **Dutch residue in the gleaner.** The clone still rejected *christus* /
  *hel*; replaced with *Kiristoos* and the שאול-seat rule.

## Hand-repaired verses (2026-09-01)

Scripts in the Selah repo hold every pair: `dev/scripts/so_hand_fixes.clj`
(the eleven), `so_hand_fixes_2.clj` (passes 2–5), `so_hand_tokens.clj`.

- **Script bleed inside fills** (Arabic, Cyrillic, Ge'ez, CJK) — *2 Sam
  21:2* ⟨أ→⟩; *Prov 1:33* ⟨bтх?⟩; *Jer 41:17* ⟨провод no—⟩; *Jer 50:38*
  ⟨ወ⟩; *Ps 150:1* ⟨в⟩ ×2; *2 Chr 4:6* ⟨в них⟩; *Deut 5:4* ⟨سى⟩; *Isa 37:20*
  ⟨аdigа⟩; *2 Kgs 12:18* ⟨对抗⟩; *Lev 14:8* a CJK gloss; *Ezek 42:10*
  ⟨איזרהта⟩ — all dropped, the Somali reads without them.
- **English articles in fills** — *Exod 21:13*, *Job 20:29*, *Lev 14:8*,
  *Ezek 40:49* (⟨the⟩ ⟨were⟩ ⟨by⟩ after five renders) — dropped; Somali has
  no article.
- **Marker + suffix left raw** (אתו / אתם / אתנו) → ⟨את⟩ + pronoun — *Zech
  11:10*, *Lev 14:24*, *Lev 24:23*, *Deut 4:19*, *Deut 26:6*, *Deut 34:6*.
- **Raw Hebrew in glosses** — *1 Chr 2:52* ⟨לְ⟩ dropped; *Deut 32:31* צור →
  **Dhagax** (twice) and a phantom ⟨את⟩ removed (the verse has none);
  *Hos 2:9* (מאהביה) and *Ps 78:35* (צור — dhagax) parentheticals dropped;
  *1 Kgs 11:5* עשתרת → Ashtoreth.
- **Translator parentheticals** (rails: none) — Ilaah-notes stripped in
  *Gen 16:13, 17:1, 21:33*, *Deut 32:30*, *Dan 7:25*, *2 Chr 11:2*; *Dan
  5:23* (Rabbiga); *Gen 30:34* (rabbigay); *2 Chr 4:6* (kiyoor) (olaca).
- **The Name** — *Gen 48:20* and *Zech 3:9* came back *Yehowah* through
  the rails three times → **Elohim** / **Yahweh** by hand.
- **Marker glyph** — ⟨אֵת⟩ / ⟨אֶת⟩ normalized to ⟨את⟩ in 4 files (glyph
  only; no marker added or removed).
- **Sentence hand-renders** — *Esther 9:11* (empty after five renders;
  nine hand tokens from the graph's surfaces), *Deut 34:6* (model
  self-talk in the sentence).
- **Token surgery** (file/graph token counts disagreed after two renders)
  — *2 Sam 5:8* a duplicated ויגע dropped; *Exod 16:29* a phantom את token
  dropped (נתן לכם השבת has none); *Deut 2:30* ולא re-joined, אלהיך → **Elohimkaaga**.

## Per-token review — the Ilaah / Rabbi floors (2026-09-01)

- **Ilaah**: 273 verses carried the word after the burn. Somali inflects it
  (*Ilaahiisa* his God, *Ilaahaaga* your God, *ilaahyada* the gods), so the
  cloned classifier — bare *Ilaah/Ilaahay* only — called 213 "garble". Read
  per token against the Hebrew seat (`dev/scripts/so_tekoa_fixes.clj`),
  mapping by the corpus's own Elohim morphology (*Elohimkaaga* 135×,
  *Elohimka* 135×, *Elohimkooda*, *Elohimkeenna* …): **67** capital-I forms on
  an אלהים-family surface with no idol word → **Elohim + suffix**
  (Ilaahiisa → Elohimkiisa); **136 lawful** (lowercase *ilaah / ilaahyo /
  ilaahyada* — the gods of the nations, idol seats — kept); **86** re-rendered
  through the rails, then 16 by hand (above). Floor after the round: 136
  lawful.
- **Rabbi**: token-level against the surfaces: **יהוה → Rabbi: 0**. The 8
  remaining are human lords (אֲדֹנִי *rabbigay*), the place-name Bath-rabbim
  (SoS 7:5), and Aramaic מרא.

## Aleph-tav audit (2026-09-01)

Graph H853/H854 indices are the truth (`dev/scripts/lang_aleph_tav_audit.clj`,
`audit :so` → `repair! :so`). First pass: 87 stray glyphs stripped, 43
sentences edited, 0 missing, **91 misaligned** (token count ≠ graph) →
re-rendered; 5 glyph-only glosses for the hand — תחת ×3 (*Exod 21:25* →
**beddel**), עם ×2 (*2 Kgs 15:38* → **la**), יתהון (*Dan 3:12* → **iyaga**),
להן (*Isa 34:17* → **iyaga**), *Zech 3:9* re-rendered. Second pass: 4
misaligned → token surgery (above). Final: **misaligned 0 · stray 0 ·
missing 0**.

## Tooling issues met on this chair

- The census/gleaner/Tekoa scripts were cloned from the Malagasy chair; three
  clone artifacts had to be fixed before the numbers could be trusted
  (`naar`, `christus|hel`, bare-form Ilaah). Every clone: fix ALL the
  language-specific literals first.
- The relay finished silently (no worker thread, count frozen) with 219
  residue — detected by a frozen count over 90 s, not by a message.
- The aleph-tav audit's positional comparison is only valid when file and
  graph token counts agree; the 91 misaligned verses show the model
  re-splitting tokens (a doubled word, a split ולא, a phantom את).

## Open for Scott

- Somali letter names for **x** and **c** in the UI catalog; π for the 314
  signature; *muraayad* for both *lens* and *mirror*.
- The Ilaah floor (136 lawful) is larger than the Dutch chair's *God* floor
  (19) because Somali's common noun for *god* is the same root as the Name-
  seat word; the split is capital-I (rejected at the seat) vs lowercase
  (lawful).
