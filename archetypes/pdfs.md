---
title: "{{ humanize .Name }}"
date: {{ .Date| time.Format "2006-01-02" }}
draft: false
toc: false
summary:
pdfurl: "/pdf/{{ .Name }}.pdf"
---

Dit artikel is te lezen als PDF-bestand:
[{{ .Name }}.pdf](/pdf/{{ .Name }}.pdf).
