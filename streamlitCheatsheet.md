# 📌 Streamlit Cheat Sheet

A quick reference for common Streamlit commands.

---

## Basic Setup
import streamlit as st

---

## Page Configuration
st.set_page_config(page_title="My App", layout="wide")

---

## Titles & Text
- st.title("This is a Title")
- st.header("This is a Header")
- st.subheader("This is a Subheader")
- st.text("This is plain text")
- st.markdown("**Markdown** _formatting_ is supported")
- st.write("Flexible display for text, numbers, DataFrames, etc.")

---

## Data Display
- st.table(data)       # Static table
- st.dataframe(data)   # Interactive table
- st.json({"key": "value"})
- st.metric(label="Temperature", value="70 °F", delta="+2 °F")

---

## Charts & Plots
- st.line_chart(data)
- st.area_chart(data)
- st.bar_chart(data)
- st.pyplot(fig)
- st.plotly_chart(fig)
- st.altair_chart(chart)

---

## Input Widgets
- st.button("Click Me")
- st.checkbox("Check me")
- st.radio("Pick one", ["A", "B", "C"])
- st.selectbox("Choose option", ["Option 1", "Option 2"])
- st.multiselect("Choose multiple", ["A", "B", "C"])
- st.slider("Slide me", 0, 100, 50)
- st.text_input("Enter text")
- st.number_input("Enter number", min_value=0, max_value=100)
- st.text_area("Enter multi-line text")
- st.date_input("Pick a date")
- st.time_input("Pick a time")
- st.file_uploader("Upload file")
- st.color_picker("Pick a color")

---

## Layouts & Containers
- col1, col2 = st.columns(2)
- col1.write("Left column")
- col2.write("Right column")

with st.expander("See details"):
    st.write("Hidden text until expanded")

- st.sidebar.title("Sidebar Title")
- st.sidebar.button("Sidebar Button")

---

## Status & Messages
- st.success("Success message")
- st.info("Info message")
- st.warning("Warning message")
- st.error("Error message")
- st.exception(Exception("Example error"))
- st.progress(50)  # 50% progress bar
- st.spinner("Loading...")

---

## Media
- st.image("image.png", caption="Example Image", use_column_width=True)
- st.audio("audio.mp3")
- st.video("video.mp4")

---

## Control Flow
- if st.button("Say hello"):
    st.write("Hello!")

---

## Caching
@st.cache_data
def load_data():
    return data

---

## Session State
- st.session_state["key"] = "value"
- st.write(st.session_state)

---

## Running the App
- streamlit run app.py
