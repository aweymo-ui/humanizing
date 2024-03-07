---
title: Transcription and Tagging
nav: Transcription
---

Another challenge of the project was the transcription element. The oral history videos consisted of 15 interviews that ranged from an hour and a half to about a half hour. The person conducting the interviews performed them with long pauses and a lot of informal speech which indicated they were resolving to edit down this material, but it never was, rendering the interview material difficult to follow if someone is listening to the recordings linearly. The CDIL’s [Oral History as Data](https://learn-static.github.io/oral-history-as-data/) or OHD offered a solution in the form of a fully visualized transcription that could be navigated by tagging and keyword searching. 

## Challenge

The problem was how to process about fifteen hours of video footage, something that would take student workers about two semesters of work to complete with the current methods. Building off of my previous work with the Washington State digital encyclopedia [HistoryLink](https://historylink.org/), I experimented with a workflow implementing [Adobe Premiere’s transcription service](https://helpx.adobe.com/premiere-pro/using/speech-to-text.html), which excelled in identifying different speakers, was much more accurate than our current transcription services and was able to be exported in almost the exact format we needed for OHD. The software also has the advantage of being able to utilize a variety of different [language packs](https://helpx.adobe.com/premiere-pro/using/download-language-packs.html), which might be very helpful in helping us fully transcribe a hispanic oral history project we are currently completing.

## Workflow

After testing a few approaches, I was able to find a method that could transcribe and an hour and a half long video in just under an hour; ten minutes to process in Premiere, five minutes to format the CSV in Google Sheets and, playing at 2x speed, proof the entire recording for errors in 45 minutes. This proofing and editing can be done ergonomically within Premier’s playback interface or directly into Visual Studio Code depending on the severity of the edits needed. In the case of these fifteen videos, I found around a 98-99% accuracy in the transcription.

Because our library has a subscription to Adobe, all of the software platforms I mentioned can be accessed by student workers. Additionally, a cheat sheet of proper names and places could be pulled from the CSV metadata for the collection the student is transcribing for quick reference while they are working through the final proof.

## Tagging with Text Mining

Another strength of OHD in providing access for listeners in what might otherwise feel like a daunting amount of runtime is the tagging capability, where threads can be woven through multiple interviews, revealing underlying themes that run throughout. To efficiently identify tag material, I dropped all of the transcript CSVs into the freely available text mining engine [Voyant](https://voyant-tools.org/). Normally, this type of text mining analysis would require some amount of “cleaning” to remove all of the ifs, ands and uhs from a document, but pulling from the “distinctive words” section of the summary can provide a similar snapshot. 

This tool looks for repeating distinctive words (compared to the rest of the corpus) separated by document. Copying this data from all fifteen transcriptions, I identified repeating tags, created a synonym list for those tags, such as wonder, profound, monumental, searched each document for these words, adding the appropriate tag into the column next to that dialogue. I found this was an efficient way to quickly survey all of the transcription material for interconnectivity and find connections that I might not be able to locate reading through the documents traditionally. 
