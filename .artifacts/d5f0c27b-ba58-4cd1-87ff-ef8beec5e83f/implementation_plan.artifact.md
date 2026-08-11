# Implementazione Nuove Funzionalità Camera e Printer

Questo piano descrive le modifiche necessarie per aggiungere un tasto di switch fotocamera, un tasto combo A+Foto e il ritaglio delle immagini della stampante.

## User Review Required

> [!IMPORTANT]
> Il tasto combo A+Foto emulerà la pressione del tasto 'A' del Game Boy. Nella maggior parte dei giochi di fotografia (come Game Boy Camera), questo triggererà lo scatto.

## Proposed Changes

### UI (Layout)

Aggiunta dei nuovi pulsanti nei layout dell'emulatore.

#### [MODIFY] [activity_gl.xml](file:///C:/Users/lucag/Documents/GitHub/gbcc-android/app/src/main/res/layout/activity_gl.xml)
#### [MODIFY] [activity_gl.xml (landscape)](file:///C:/Users/lucag/Documents/GitHub/gbcc-android/app/src/main/res/layout-land/activity_gl.xml)

- Aggiunta di `buttonCameraSwitch` (ImageButton).
- Aggiunta di `buttonAPhoto` (ImageButton).

---

### Logic (Kotlin)

Implementazione della logica di gestione camera e ritaglio stampante.

#### [MODIFY] [GLActivity.kt](file:///C:/Users/lucag/Documents/GitHub/gbcc-android/app/src/main/java/com/philj56/gbcc/GLActivity.kt)

- Gestione del ciclo delle fotocamere disponibili tramite `CameraX`.
- Implementazione del listener per lo switch della fotocamera.
- Implementazione del listener per il tasto combo A+Foto.
- Modifica della logica di esportazione della stampante per applicare il ritaglio (16px sopra, 48px sotto).
- Visualizzazione dei nuovi tasti solo se `isCamera()` è vero.

## Verification Plan

### Automated Tests
- Non applicabile direttamente senza hardware specifico, ma verificherò la compilazione.

### Manual Verification
- Avvio dell'app con una ROM che supporta la camera (es. Game Boy Camera).
- Verifica della presenza dei nuovi pulsanti.
- Test dello switch tra le varie fotocamere dello smartphone.
- Test del tasto combo A+Foto.
- Stampa di un'immagine e verifica del ritaglio nel file salvato.
