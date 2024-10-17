# Lab1
# reading from audio and textgrid files
audio = Read from file: "C:\Users\furgesc\Downloads\sample1.wav"
textGrid = Read from file: "C:\Users\furgesc\Downloads\sample1.TextGrid"

selectObject: textGrid

numberIntervals = Get number of intervals: 1

for i from 1 to numberIntervals
	intStartTime = Get start time of interval: 1, i
	intEndTime = Get end time of interval: 1, i
	intDuration = intEndTime - intStartTime
	thisPhoneme$ = Get label of interval: 1, i

	appendInfoLine: "Interval ", i, ": Vowel: ", thisPhoneme$, " Start: ", intStartTime, " End: ", intEndTime, " Duration: ", intDuration
endfor
