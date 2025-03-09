import streamlit as st
from PIL import Image

# Title for the web app
st.title("AI-powered Waste Sorting System")

# Description of the app
st.write("""
This app classifies waste images and provides suggestions for proper disposal.
Upload an image of waste to get started!
""")

# File uploader widget
uploaded_image = st.file_uploader("Choose a waste image...", type=["jpg", "jpeg", "png"])

# If an image is uploaded, show it
if uploaded_image is not None:
    # Open the image using PIL
    image = Image.open(uploaded_image)
    
    # Display the uploaded image
    st.image(image, caption="Uploaded Waste Image", use_column_width=True)
    
    # Placeholder for classification logic (update with your Groq integration)
    st.write("Classification Result: [Waste Type]")

    # Placeholder for bin location suggestion (Sampleapp.ai integration)
    st.write("Nearest bin location: [API Result Here]")


