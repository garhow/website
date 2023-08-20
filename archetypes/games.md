---
draft: true
date: {{ .Date }}
resources:
- name: cover
  src: cover.png
title: "{{ replace .Name "-" " " | title }}"
release_date: {{ now.Format "2006-01-02" }}
platforms:
- ""
developers: 
- ""
publishers:
- ""
series: ""
genres: [""]
played: false
play_date: {{ now.Format "2006-01-02" }}
completed: false
completion_date: {{ now.Format "2006-01-02" }}
mastered: false
mastery_date: {{ now.Format "2006-01-02" }}
rating: 5 # out of 10
---

