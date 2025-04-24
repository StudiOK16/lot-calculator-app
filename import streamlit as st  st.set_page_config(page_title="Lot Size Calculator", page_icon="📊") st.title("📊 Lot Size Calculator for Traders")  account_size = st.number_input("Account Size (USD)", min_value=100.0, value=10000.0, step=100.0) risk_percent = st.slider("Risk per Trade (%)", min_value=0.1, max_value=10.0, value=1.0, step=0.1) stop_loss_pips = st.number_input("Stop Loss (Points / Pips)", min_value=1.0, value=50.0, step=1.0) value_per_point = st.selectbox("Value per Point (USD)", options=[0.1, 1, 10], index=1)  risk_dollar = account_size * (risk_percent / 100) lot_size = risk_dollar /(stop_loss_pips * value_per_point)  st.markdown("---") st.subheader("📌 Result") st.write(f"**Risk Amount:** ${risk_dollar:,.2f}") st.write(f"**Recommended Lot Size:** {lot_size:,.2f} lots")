import streamlit as st

st.set_page_config(page_title="Lot Size Calculator", page_icon="📊")
st.title("📊 Lot Size Calculator for Traders")

account_size = st.number_input("Account Size (USD)", min_value=100.0, value=10000.0, step=100.0)
risk_percent = st.slider("Risk per Trade (%)", min_value=0.1, max_value=10.0, value=1.0, step=0.1)
stop_loss_pips = st.number_input("Stop Loss (Points / Pips)", min_value=1.0, value=50.0, step=1.0)
value_per_point = st.selectbox("Value per Point (USD)", options=[0.1, 1, 10], index=1)

risk_dollar = account_size * (risk_percent / 100)
lot_size = risk_dollar / (stop_loss_pips * value_per_point)

st.markdown("---")
st.subheader("📌 Result")
st.write(f"**Risk Amount:** ${risk_dollar:,.2f}")
st.write(f"**Recommended Lot Size:** {lot_size:,.2f} lots")
