# Waste-Management
import streamlit as st

# Title for the web app
st.title("AI-powered Waste Sorting System")

# Description of the app
st.write("""
This app classifies waste images and provides suggestions for proper disposal. Upload an image of waste to get started!
""")

# File uploader widget
uploaded_image = st.file_uploader("Choose a waste image...", type="jpg")

# If an image is uploaded, show it
if uploaded_image is not None:
    st.image(uploaded_image, caption="Uploaded Waste Image", use_column_width=True)

    # Here you would call your AI model to classify the uploaded image.
    # Placeholder for classification logic (update with your Groq integration)
    st.write("Classification Result: [Waste Type]")

    # Example placeholder for bin location suggestion
    st.write("Nearest bin location: [API Result Here]")

