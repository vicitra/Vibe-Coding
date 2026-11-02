# 🎸 Tone Finder

Pagina web (un solo file, nessuna installazione) che ti dice come regolare **la tua** attrezzatura per avvicinarti al suono di una canzone:

- **Hamer Slammer Series (Californian)**: HSS, Floyd Rose, selettore a 5 posizioni
- **Takamine G Series**: elettroacustica cutaway con preamp
- **M-VAVE Cube Baby AC**: multieffetto per acustica
- **Fender Super Champ XD**: 2 canali, 16 Voice, 16 effetti

## Come si usa

1. Apri `index.html` nel browser (doppio clic).
2. Scrivi `Band - Titolo` oppure incolla un link YouTube/Spotify.
3. Scegli **Elettrica** o **Acustica** e premi **Trova il suono**.

### Due motori

| Motore | Cosa fa | Serve |
|---|---|---|
| **AI** | Claude cerca sul web l'attrezzatura originale del brano (chitarra, ampli, effetti, accordatura) e la traduce nella tua | una chiave API Anthropic (console.anthropic.com) |
| **Offline** | Riconosce artista/brano da un database interno (~200 artisti, brani famosi con note specifiche) e applica uno stile | niente |

La chiave API resta solo nel tuo browser (localStorage) e va solo ad `api.anthropic.com`. **Non scriverla mai nel codice e non caricarla su GitHub.**

Il risultato mostra i knob del Super Champ XD (i knob del canale non usato sono in grigio), la posizione del pickup o l'EQ della Takamine, i parametri della Cube Baby AC e i consigli di tecnica. Il pulsante 📋 copia tutto come testo.
