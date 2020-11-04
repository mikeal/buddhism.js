# buddhism.js

Buddhist concepts as JavaScript

## Pratītyasamutpāda (Dependent Origination)

Basic principals.

```js
const a = (_this, that) => {
  if (_this) that()
}
const b = (that) => {
  const _this = false
  // vm knows this will never be called, this code can be dropped
  // and will never exist
  if (_this) that()
}
const c = (_this) => {
  const that = false
  // vm knows this will never be called, this code can be dropped
  // and will never exist
  if (that && _this) return _this
}
```

### Twelve-fold chain

![Centro_2](https://user-images.githubusercontent.com/579/98151375-e9aede80-1e84-11eb-80f3-06cb9468c6f3.jpg)

As a loop.

```js
// Avijjā (Ignorance)
const avijja = (...args) => sankhara(...args)

// Saṅkhāra (Conditioning)
const sankhara = (...args) => vinnana(...args)

// Viññāṇa (Consciousness)
const vinnana = (...args) => namarupa(...args)

// Nāmarūpa (Name & Form)
const namarupa = (...args) => salayatana(...args)

// Saḷāyatana (Six Sense Bases)
const salayatana = (...args) => phassa(...args)

// Phassa (Contact)
const phassa = (...args) => vedana(...args)

// Vedanā (Sensation)
const vedana = (...args) => tanha(...args)

// Taṇhā (Craving)
const tanha = (...args) => upadana(...args)

// Upādāna (Clinging)
const upadana = (...args) => bhava(...args)

// Bhava (Being)
const bhava = (...args) => jati(...args)

// Jāti (Birth)
const jati = (...args) => jaramarana(...args)

// Jarāmaraṇa (Old Age & Death)
const jaramarana = (...args) => avijja(...args)
```
