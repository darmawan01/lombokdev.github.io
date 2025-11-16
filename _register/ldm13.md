---
layout: register
title: Lombok Dev Meetup #13 Registration
api_url: "https://example.com/api/register"
open_at: 2025-11-01
closed_at: 2025-12-20
event_id: 76c97414-dc19-4e8c-9c99-b90b7d1c5a91

forms:
  - title: Phone Number
    name: phone
    type: text
    required: true
    placeholder: "+62 812-3456-7890"
  - title: Gender
    name: gender
    type: options
    required: false
    options: ["male", "female"]
  - title: Occupation
    name: occupation
    type: options
    required: true
    options: ["Student", "Working Professional", "Freelancer", "Entrepreneur", "Other"]
  - title: Job Title
    name: job_title
    type: text
    required: false
    placeholder: "e.g., Software Engineer, Frontend Developer"
    condition: "occupation == 'Working Professional' || occupation == 'Freelancer'"
  - title: Company
    name: company
    type: text
    required: false
    placeholder: "Company or Organization name"
    condition: "occupation == 'Working Professional' || occupation == 'Freelancer'"
  - title: School/University
    name: school
    type: text
    required: false
    placeholder: "School or University name"
    condition: "occupation == 'Student'"
  - title: Interesting Topic
    name: interest_topic
    type: options
    required: true
    options: ["Backend Development", "Frontend Development", "DevOps", "Mobile Development", "AI/ML", "Data Science", "Cloud Computing", "Security", "UI/UX Design", "Other"]
  - title: How did you find this event?
    name: event_source
    type: options
    required: true
    options: ["Social Media (Instagram/Facebook)", "Twitter/X", "LinkedIn", "Friend/Colleague", "Website", "Email Newsletter", "Previous Event", "Other"]
  - title: Agreement
    name: agreement
    type: check
    required: true
    details: By checking this, you agree with our terms and conditions (https://term.condition)
---

