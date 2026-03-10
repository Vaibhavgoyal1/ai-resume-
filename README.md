# ai-resume-import streamlit as st

st.title("AI Resume Analyzer")

resume = st.text_area("Paste your Resume")

job_desc = st.text_area("Paste Job Description")

if st.button("Analyze"):
    score = len(set(resume.split()) & set(job_desc.split()))
    st.write("ATS Match Score:", score)
