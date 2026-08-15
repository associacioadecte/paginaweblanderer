# Imatges i logo pendents — landerer.adecte.cat

El fitxer `index.html` ja està preparat per mostrar aquestes imatges automàticament
en quant les afegiu a la mateixa carpeta (amb el mateix nom de fitxer). Mentre no
hi siguin, es veu un requadre de color amb el nom del fitxer esperat, així que la
web ja es pot revisar sense que es vegin icones d'imatge trencada.

## 1. Logos

| Fitxer | On es fa servir | Recomanacions |
|---|---|---|
| `logo-landerer.png` | Capçalera (petit), secció principal / hero (gran), peu de pàgina (petit) | PNG amb fons transparent, format quadrat o proper, mínim 500×500 px |
| `idece.png` | Secció «Amb el suport de:», sobre el peu de pàgina | PNG amb fons transparent, alçada visible ~56px, sense marges blancs sobrants |

Cal pujar-los a la mateixa carpeta que `index.html` (arrel del lloc).

## 2. Galeria de la missió (secció «La missió en imatges»)

Carpeta `images/`:

| Fitxer | Contingut |
|---|---|
| `images/preparacio-globus.jpg` | Foto de l'equip preparant el globus abans del llançament |
| `images/enlairament.jpg` | Foto o fotograma del moment de l'enlairament / ascens del globus |
| `images/equip-terres-ebre.jpg` | Foto de l'equip de Landerer / ADECTE a les Terres de l'Ebre |
| `images/vista-estratosfera.jpg` | Imatge captada per la càpsula durant el vol (vista des de l'estratosfera), si en teniu |

## 3. Càpsules dels centres educatius (secció «Una càpsula per a cada centre»)

Carpeta `images/`:

| Fitxer | Centre |
|---|---|
| `images/capsula-daniel-mangrane.jpg` | IE Daniel Mangrané |
| `images/capsula-dertosa.jpg` | INS Dertosa |
| `images/capsula-roquetes.jpg` | Institut Roquetes |
| `images/capsula-terra-alta.jpg` | Institut Terra Alta |

Foto de la càpsula construïda pel centre, o de l'alumnat treballant-hi.

## Recomanacions tècniques

- Format: JPG o WebP.
- Relació d'aspecte: 4:3 (horitzontal), mínim 1200–1600 px d'amplada.
- Pes optimitzat, per sota de 400 KB per imatge si és possible, perquè la web carregui ràpid.

## Estructura de carpetes esperada

```
/ (arrel del lloc)
├── index.html
├── logo-landerer.png
├── idece.png
├── press-kit.zip
└── images/
    ├── preparacio-globus.jpg
    ├── enlairament.jpg
    ├── equip-terres-ebre.jpg
    ├── vista-estratosfera.jpg
    ├── capsula-daniel-mangrane.jpg
    ├── capsula-dertosa.jpg
    ├── capsula-roquetes.jpg
    └── capsula-terra-alta.jpg
```

## Kit de premsa

El botó «Descarregar Kit de Premsa» (secció «El projecte, per dins») enllaça amb
`press-kit.zip`, a l'arrel del lloc, al costat de `index.html`. Recomanem que
contingui: logotips en alta resolució, fotografies de la missió amb drets d'ús
autoritzats, i una fitxa tècnica breu del projecte.

## Xarxes socials d'ADECTE

Al peu de pàgina hi ha tres icones (Instagram, X/Twitter, YouTube) que ara mateix
enllacen a `#` com a placeholder. Cerqueu-los al codi (comentari `<!-- Substituïu
aquests href="#" -->` just abans del bloc `foot-social` a `index.html`) i
substituïu-los per les URL reals dels perfils d'ADECTE. Si alguna xarxa no
existeix, simplement elimineu el seu `<a>` corresponent.

## Compte enrere

Ara mateix el compte enrere mostra «Data encara per confirmar». Quan tingueu la
data oficial de la propera missió:

1. Obriu `index.html`.
2. Cerqueu `const LAUNCH_DATE = null;` (a prop del final del fitxer, dins del `<script>`).
3. Substituïu-ho per la data real, per exemple:
   ```js
   const LAUNCH_DATE = new Date('2026-11-14T10:00:00+01:00');
   ```
   (`+01:00` en horari d'hivern, `+02:00` en horari d'estiu — hora de Catalunya).
4. Deseu el fitxer. El compte enrere s'activa automàticament, sense cap altre canvi.
