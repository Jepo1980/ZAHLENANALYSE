
import streamlit as st
from collections import Counter

# Integrierte Nachfolgerdaten basierend auf Seed 206555
nachfolger_daten = {
    0: 17, 1: 35, 2: 5, 3: 4, 4: 4, 5: 16, 6: 21, 7: 32, 8: 14, 9: 35, 
    10: 6, 11: 20, 12: 17, 13: 25, 14: 32, 15: 35, 16: 28, 17: 11, 18: 33, 
    19: 29, 20: 15, 21: 35, 22: 14, 23: 11, 24: 30, 25: 8, 26: 20, 27: 12, 
    28: 3, 29: 24, 30: 14, 31: 10, 32: 5, 33: 22, 34: 28, 35: 5, 36: 17
}

st.title("Automatisierte Nachfolgeranalyse")

st.write("### Bisher bekannte Nachfolgerzahlen")
st.write(nachfolger_daten)

# Eingabe der gefallenen Zahlen
st.write("### Gefallene Zahlen eingeben")
user_input = st.text_input("Gib die gefallenen Zahlen durch Kommas getrennt ein:", "5, 2, 30, 8")
zahlen_liste = [int(x.strip()) for x in user_input.split(",") if x.strip().isdigit()]

if zahlen_liste:
    st.write("### Deine Eingabe")
    st.write(zahlen_liste)

    # Analyse der Nachfolger basierend auf den Eingaben
    combined_successors = Counter()
    for zahl in zahlen_liste:
        if zahl in nachfolger_daten:
            nachfolger = nachfolger_daten[zahl]
            combined_successors[nachfolger] += 1

    if combined_successors:
        wahrscheinlichste_zahl, haeufigkeit = combined_successors.most_common(1)[0]
        st.write("### Wahrscheinlichste nächste Zahl:")
        st.write(f"**Zahl:** {wahrscheinlichste_zahl}, **Häufigkeit:** {haeufigkeit}")
    else:
        st.write("Keine Nachfolgeranalyse möglich - überprüfe die Eingabe.")
