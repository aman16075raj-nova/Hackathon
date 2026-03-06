campuscare-platform/

README.md
requirements.txt
.gitignore

docs/
problem-statement.md
system-design.md
presentation-notes.md

src/
app.py
hostel_module.py
dining_module.py
mental_health_module.py

data/
rooms.json
menu.json
feedback.json
Prototype Interface (Python + Streamlit)
import streamlit as st
from hostel_module import hostel_dashboard
from dining_module import dining_dashboard
from mental_health_module import mental_dashboard

st.title("CampusCare - Student Life & Well-being")

menu = ["Hostel Life", "Dining System", "Mental Health"]

choice = st.sidebar.selectbox("Select Module", menu)

if choice == "Hostel Life":
    hostel_dashboard()

elif choice == "Dining System":
    dining_dashboard()

elif choice == "Mental Health":
    mental_dashboard()
import streamlit as st

def hostel_dashboard():

    st.header("Hostel Life Management")

    tab1, tab2, tab3, tab4 = st.tabs([
        "Room Selection",
        "Maintenance & Cleaning",
        "Roommate Issues",
        "Feedback"
    ])

    with tab1:
        st.subheader("Choose Your Room")
        room_type = st.selectbox(
            "Room Type",
            ["Single", "Double", "Triple"]
        )
        floor = st.selectbox(
            "Preferred Floor",
            ["Ground", "1st", "2nd", "3rd"]
        )

        if st.button("Submit Room Preference"):
            st.success("Room preference submitted")

    with tab2:
        st.subheader("Cleaning / Maintenance Request")
        issue = st.selectbox(
            "Issue Type",
            ["Bathroom Cleaning", "Room Cleaning", "Plumbing", "Electric"]
        )

        desc = st.text_area("Describe issue")

        if st.button("Report Issue"):
            st.success("Maintenance request sent")

    with tab3:
        st.subheader("Roommate Problem Resolution")

        problem = st.text_area("Describe the issue")

        if st.button("Submit Complaint"):
            st.success("Hostel authority notified")

    with tab4:
        st.subheader("Feedback")

        facility = st.selectbox(
            "Select facility",
            ["Hostel Staff", "Cleaning Service", "Security", "Wardens"]
        )

        rating = st.slider("Rate", 1, 5)

        if st.button("Submit Feedback"):
            st.success("Feedback recorded")
import streamlit as st

def dining_dashboard():

    st.header("Dining System")

    cuisine = st.selectbox(
        "Select Cuisine",
        [
            "North Indian",
            "South Indian",
            "Punjabi",
            "Gujarati",
            "Bengali",
            "Italian",
            "Chinese",
            "Mexican"
        ]
    )

    meal = st.selectbox(
        "Meal Type",
        ["Breakfast", "Lunch", "Dinner"]
    )

    preferred = st.text_input("Preferred Food Item")

    if st.button("Reserve Meal"):
        st.success("Meal reserved")

    st.subheader("Backup Meal Option")

    backup = st.selectbox(
        "Select Backup Meal",
        [
            "Veg Thali",
            "Rice + Dal",
            "Chapati + Sabzi",
            "Pasta",
            "Noodles"
        ]
    )

    if st.button("Confirm Backup"):
        st.success("Backup option saved")
import streamlit as st

def mental_dashboard():

    st.header("Mental Health Resources")

    tab1, tab2, tab3 = st.tabs([
        "Self Help Tools",
        "Talk to Counselor",
        "Peer Support"
    ])

    with tab1:
        st.write("Stress Management Tools")
        mood = st.slider("How are you feeling today?", 1, 10)

        if st.button("Submit Mood"):
            st.success("Mood recorded")

    with tab2:
        st.write("Book appointment with counselor")

        day = st.selectbox(
            "Select Day",
            ["Monday", "Tuesday", "Wednesday"]
        )

        if st.button("Book Session"):
            st.success("Counseling session booked")

    with tab3:
        st.write("Peer Support Groups")

        group = st.selectbox(
            "Choose group",
            [
                "Academic Stress",
                "Homesickness",
                "Social Anxiety"
            ]
        )

        if st.button("Join Group"):
            st.success("Group joined")
