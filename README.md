# counter-app.py
counter app
import streamlit as st

st.title("Counter App")

# Ensure session state for the counter
if "count" not in st.session_state:
    st.session_state.count = 0

st.write(f"### Current Count: {st.session_state.count}")

# Increment and decrement functions
def increment():
    st.session_state.count += 1

def decrement():
    st.session_state.count -= 1

# Buttons with working state
col1, col2 = st.columns(2)

col1.button("➕ Increment", on_click=increment)
col2.button("➖ Decrement", on_click=decrement)
