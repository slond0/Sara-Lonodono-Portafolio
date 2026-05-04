# -*- coding: utf-8 -*-
import streamlit as st

st.set_page_config(
    page_title="Galeria - Portafolio Streamlit",
    page_icon="\U0001f3a8",
    layout="wide",
)

APPS = [
    {"num": "01", "title": "Traductor de Texto",       "cat": "NLP - Traduccion",    "tag": "nlp",        "icon": "\U0001f310", "url": "https://traductor-1.streamlit.app/"},
    {"num": "02", "title": "App de Audio",             "cat": "Audio - NLP",         "tag": "audio nlp",  "icon": "\U0001f50a", "url": "https://audio1.streamlit.app/"},
    {"num": "03", "title": "Una App",                  "cat": "IA General",          "tag": "ia",         "icon": "\U0001f9e9", "url": "https://unaapp.streamlit.app/"},
    {"num": "04", "title": "Proyecto Demo",            "cat": "IA General",          "tag": "ia",         "icon": "\u26a1",     "url": "https://aaaaaa2.streamlit.app/"},
    {"num": "05", "title": "Traductor de Imagenes",    "cat": "NLP - Vision",        "tag": "nlp vision", "icon": "\U0001f5bc", "url": "https://traductorimg.streamlit.app/"},
    {"num": "06", "title": "Analisis de Sentimientos", "cat": "NLP - Sentimientos",  "tag": "nlp",        "icon": "\U0001f4ac", "url": "https://sentimenta-1.streamlit.app/"},
    {"num": "07", "title": "TF-IDF Espanol",           "cat": "NLP - TF-IDF",        "tag": "nlp",        "icon": "\U0001f4ca", "url": "https://tdfesp-1.streamlit.app/"},
    {"num": "08", "title": "Demo TF-IDF",              "cat": "NLP - Demo",          "tag": "nlp",        "icon": "\U0001f4c8", "url": "https://demotfidf.streamlit.app/"},
    {"num": "09", "title": "Detector de Imagenes",     "cat": "Vision - Deteccion",  "tag": "vision",     "icon": "\U0001f50d", "url": "https://detectorimagen.streamlit.app/"},
    {"num": "10", "title": "Traductor Avanzado",       "cat": "NLP - Traduccion",    "tag": "nlp",        "icon": "\U0001f30d", "url": "https://traductor-adawr4aw5ks5l2kmzy4zpq.streamlit.app/"},
    {"num": "11", "title": "YOLOv5 Detector",          "cat": "Vision - YOLO",       "tag": "vision",     "icon": "\U0001f3af", "url": "https://yolov51.streamlit.app/"},
    {"num": "12", "title": "Receptor MQTT",            "cat": "IoT - MQTT",          "tag": "iot",        "icon": "\U0001f4e1", "url": "https://recepmqtt-d2pzpesymrkowp3ptyegrs.streamlit.app/"},
    {"num": "13", "title": "Emisor MQTT",              "cat": "IoT - MQTT",          "tag": "iot",        "icon": "\U0001f4e4", "url": "https://sendcmqtt-1.streamlit.app/"},
    {"num": "14", "title": "Control por Voz",          "cat": "Audio - IoT",         "tag": "audio iot",  "icon": "\U0001f3a4", "url": "https://ctrlvoice1.streamlit.app/"},
    {"num": "15", "title": "Reconocimiento Digitos",   "cat": "Vision - IA",         "tag": "vision ia",  "icon": "\U0001f522", "url": "https://reconocimientodigitos1.streamlit.app/"},
    {"num": "16", "title": "Reconocimiento Dibujos",   "cat": "Vision - Dibujo",     "tag": "vision ia",  "icon": "\u270f",     "url": "https://drawrecogni.streamlit.app/"},
    {"num": "17", "title": "Historias Infantiles",     "cat": "IA - Generativa",     "tag": "ia nlp",     "icon": "\U0001f4d6", "url": "https://historiasinfantiles.streamlit.app/"},
    {"num": "18", "title": "Vision App",               "cat": "Vision - IA",         "tag": "vision ia",  "icon": "\U0001f441", "url": "https://visionapp-cdll4scmlpnggnnh4m5qjf.streamlit.app/"},
    {"num": "19", "title": "Chat con PDF",             "cat": "NLP - Documentos",    "tag": "nlp ia",     "icon": "\U0001f4c4", "url": "https://chatpdf1.streamlit.app/"},
    {"num": "20", "title": "LSTM NLP",                 "cat": "NLP - Deep Learning", "tag": "nlp ia",     "icon": "\U0001f9e0", "url": "http://lstmnlp-pq3hqydqdi7mdegdcrw3fg.streamlit.app/"},
]

CATEGORIES = {
    "Todas":       "all",
    "NLP & Texto": "nlp",
    "Vision":      "vision",
    "IoT & MQTT":  "iot",
    "Audio":       "audio",
    "IA General":  "ia",
}

CSS = """
<style>
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=DM+Mono:wght@300;400&family=Cormorant+Garamond:wght@300;400;600&display=swap');
html, body, [data-testid="stAppViewContainer"] { background: #0a0a08 !important; color: #f5f0e8; }
[data-testid="stHeader"],[data-testid="stToolbar"],[data-testid="stDecoration"],footer { display:none !important; }
[data-testid="stAppViewContainer"] { padding: 0 !important; }
.block-container { padding: 0 !important; max-width: 100% !important; }
.gal-header { padding:64px 60px 40px; border-bottom:1px solid #2a2a26; display:flex; justify-content:space-between; align-items:flex-end; gap:32px; flex-wrap:wrap; }
.gal-label { font-family:'DM Mono',monospace; font-size:10px; letter-spacing:.3em; color:#c9a84c; text-transform:uppercase; margin-bottom:14px; }
.gal-h1 { font-family:'Playfair Display',serif; font-size:clamp(2.6rem,5vw,5rem); font-weight:400; line-height:1.05; color:#f0ead8; letter-spacing:-.02em; margin:0; }
.gal-h1 em { font-style:italic; color:#e2c278; }
.gold-line { width:60px; height:1px; background:#c9a84c; margin:18px 0; }
.gal-sub { font-family:'DM Mono',monospace; font-size:11px; color:#6b6b5e; letter-spacing:.08em; line-height:1.8; max-width:420px; }
.gal-count-label { font-family:'DM Mono',monospace; font-size:9px; letter-spacing:.25em; color:#6b6b5e; text-transform:uppercase; margin-bottom:6px; text-align:right; }
.gal-count-num { font-family:'Playfair Display',serif; font-size:5rem; color:#2a2a26; line-height:1; font-style:italic; text-align:right; }
.filter-bar { padding:20px 60px; border-bottom:1px solid #2a2a26; display:flex; align-items:center; gap:16px; flex-wrap:wrap; }
.filter-label-txt { font-family:'DM Mono',monospace; font-size:9px; letter-spacing:.3em; color:#6b6b5e; text-transform:uppercase; }
.stRadio > div { flex-direction:row !important; gap:8px !important; flex-wrap:wrap; }
.stRadio label { padding:5px 14px !important; border:1px solid #2a2a26 !important; background:transparent !important; color:#6b6b5e !important; font-family:'DM Mono',monospace !important; font-size:10px !important; letter-spacing:.15em !important; cursor:pointer !important; border-radius:0 !important; transition:all .2s !important; }
.stRadio label:hover { border-color:#c9a84c !important; color:#c9a84c !important; }
.stRadio [aria-checked="true"] label { border-color:#c9a84c !important; color:#c9a84c !important; background:rgba(201,168,76,.07) !important; }
.stats-bar { padding:12px 60px; background:#0e0e0c; border-bottom:1px solid #1a1a18; font-family:'DM Mono',monospace; font-size:10px; letter-spacing:.2em; color:#6b6b5e; text-transform:uppercase; }
.stats-bar span { color:#c9a84c; }
.gallery-wrap { padding:48px 60px 60px; }
.app-card { background:#161614; border:1px solid #2a2a26; transition:border-color .25s,transform .2s,box-shadow .2s; overflow:hidden; cursor:pointer; text-decoration:none !important; display:block; }
.app-card:hover { border-color:#c9a84c; transform:translateY(-3px); box-shadow:0 12px 40px rgba(0,0,0,.65); text-decoration:none !important; }
.card-preview { height:185px; background:#111110; display:flex; flex-direction:column; align-items:center; justify-content:center; gap:10px; position:relative; overflow:hidden; }
.card-icon { font-size:3rem; opacity:.5; transition:opacity .25s; }
.app-card:hover .card-icon { opacity:.9; }
.card-preview-label { font-family:'DM Mono',monospace; font-size:9px; letter-spacing:.22em; color:#6b6b5e; text-transform:uppercase; padding:0 16px; text-align:center; }
.card-num { position:absolute; top:10px; left:10px; background:#0a0a08; border:1px solid #2a2a26; color:#6b6b5e; font-family:'DM Mono',monospace; font-size:9px; letter-spacing:.2em; padding:3px 8px; }
.card-preview::after { content:''; position:absolute; inset:0; background:linear-gradient(135deg,rgba(201,168,76,.09) 0%,transparent 60%); opacity:0; transition:opacity .3s; pointer-events:none; }
.app-card:hover .card-preview::after { opacity:1; }
.card-hover-overlay { position:absolute; inset:0; background:rgba(10,10,8,.82); display:flex; align-items:center; justify-content:center; opacity:0; transition:opacity .25s; }
.app-card:hover .card-hover-overlay { opacity:1; }
.visit-btn-inner { border:1px solid #c9a84c; color:#c9a84c; padding:9px 24px; font-family:'DM Mono',monospace; font-size:10px; letter-spacing:.3em; text-transform:uppercase; }
.card-footer { padding:16px 18px 18px; border-top:1px solid #2a2a26; display:flex; align-items:flex-start; justify-content:space-between; gap:10px; }
.card-cat { font-family:'DM Mono',monospace; font-size:9px; letter-spacing:.25em; color:#c9a84c; text-transform:uppercase; margin-bottom:5px; }
.card-title-txt { font-family:'Cormorant Garamond',serif; font-size:1.18rem; font-weight:600; color:#f0ead8; line-height:1.2; }
.card-url-txt { font-family:'DM Mono',monospace; font-size:8px; color:#4a4a40; margin-top:5px; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; max-width:220px; }
.card-arrow { color:#c9a84c; font-size:1.1rem; padding-top:4px; flex-shrink:0; }
.gal-footer { border-top:1px solid #2a2a26; padding:32px 60px; display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:12px; margin-top:16px; }
.footer-brand { font-family:'Playfair Display',serif; font-size:1rem; color:#c9a84c; font-style:italic; }
.footer-meta { font-family:'DM Mono',monospace; font-size:10px; letter-spacing:.2em; color:#6b6b5e; text-transform:uppercase; }
@media (max-width:768px) {
    .gal-header,.filter-bar,.stats-bar,.gallery-wrap,.gal-footer { padding-left:18px !important; padding-right:18px !important; }
    .gal-h1 { font-size:2.2rem !important; }
}
</style>
"""

st.markdown(CSS, unsafe_allow_html=True)

total = len(APPS)
st.markdown(
    "<div class='gal-header'>"
    "<div>"
    "<div class='gal-label'>Portafolio &middot; Streamlit Cloud</div>"
    "<h1 class='gal-h1'>La <em>Galeria</em><br>de Aplicaciones</h1>"
    "<div class='gold-line'></div>"
    "<p class='gal-sub'>Una coleccion curada de aplicaciones web construidas con Streamlit.<br>"
    "Haz clic en cualquier obra para visitarla en una nueva pestana.</p>"
    "</div>"
    "<div>"
    "<div class='gal-count-label'>Obras en exposicion</div>"
    f"<div class='gal-count-num'>{total}</div>"
    "</div>"
    "</div>",
    unsafe_allow_html=True,
)

st.markdown("<div class='filter-bar'><span class='filter-label-txt'>Coleccion &middot;&nbsp;&nbsp;</span>", unsafe_allow_html=True)
selected_label = st.radio(
    label="Filtrar",
    options=list(CATEGORIES.keys()),
    horizontal=True,
    label_visibility="collapsed",
)
selected_tag = CATEGORIES[selected_label]
st.markdown("</div>", unsafe_allow_html=True)

filtered = [a for a in APPS if selected_tag == "all" or selected_tag in a["tag"]]

st.markdown(
    "<div class='stats-bar'>"
    f"Mostrando <span>{len(filtered)}</span> de <span>{total}</span> obras"
    f" &nbsp;&middot;&nbsp; Categoria: <span>{selected_label}</span>"
    "</div>",
    unsafe_allow_html=True,
)

st.markdown("<div class='gallery-wrap'>", unsafe_allow_html=True)

COLS = 3
rows = [filtered[i:i + COLS] for i in range(0, len(filtered), COLS)]

for row in rows:
    cols = st.columns(len(row), gap="small")
    for col, app in zip(cols, row):
        with col:
            domain = app["url"].replace("https://", "").replace("http://", "").rstrip("/")
            html = (
                "<a class='app-card' href='" + app["url"] + "' target='_blank' rel='noopener noreferrer'>"
                "<div class='card-preview'>"
                "<div class='card-num'>" + app["num"] + "</div>"
                "<div class='card-icon'>" + app["icon"] + "</div>"
                "<div class='card-preview-label'>" + app["title"] + "</div>"
                "<div class='card-hover-overlay'><div class='visit-btn-inner'>Visitar &#8594;</div></div>"
                "</div>"
                "<div class='card-footer'>"
                "<div style='min-width:0; flex:1;'>"
                "<div class='card-cat'>" + app["cat"] + "</div>"
                "<div class='card-title-txt'>" + app["title"] + "</div>"
                "<div class='card-url-txt'>" + domain + "</div>"
                "</div>"
                "<div class='card-arrow'>&#8599;</div>"
                "</div>"
                "</a>"
            )
            st.markdown(html, unsafe_allow_html=True)

st.markdown("</div>", unsafe_allow_html=True)

st.markdown(
    "<div class='gal-footer'>"
    "<span class='footer-brand'>Galeria Streamlit</span>"
    f"<span class='footer-meta'>{total} aplicaciones &middot; Streamlit Cloud &middot; 2025</span>"
    "</div>",
    unsafe_allow_html=True,
)
