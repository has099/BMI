import streamlit as st

st.set_page_config(page_title="حاسبة مؤشر كتلة الجسم", page_icon="⚖️", layout="centered")

st.title("⚖️ حاسبة مؤشر كتلة الجسم (BMI)")
st.write("احسب مؤشر كتلة جسمك للتعرف على فئة وزنك الحالية.")

st.divider()

weight = st.number_input("الوزن (كغم):", min_value=30.0, max_value=200.0, value=70.0, step=0.5)
height_cm = st.number_input("الطول (سم):", min_value=100.0, max_value=220.0, value=170.0, step=1.0)

if st.button("🚀 احسب المؤشر الآن", type="primary"):
    height_m = height_cm / 100
    bmi = weight / (height_m ** 2)
    
    st.success("تم الحساب بنجاح!")
    st.metric("مؤشر كتلة الجسم (BMI)", round(bmi, 1))
    
    if bmi < 18.5:
        st.info("💡 الفئة: **نقص في الوزن**")
    elif 18.5 <= bmi < 25:
        st.success("💡 الفئة: **وزن مثالي وصحي**")
    elif 25 <= bmi < 30:
        st.warning("💡 الفئة: **زيادة في الوزن**")
    else:
        st.error("💡 الفئة: **سمنة**")
