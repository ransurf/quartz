
# 2022-03 Week 13

[[2022 Week 12|↶ Previous Week]] | [[2022 Week 14|Following Week ↷]]

**Metadata:**
- Created:: 2022-03-31 @ 20:02
- Tags:: #calendar/weekly/2022

**Table of Contents:**
```toc
style: number
```

___

### Summary
- [[dailyNotes/2022-03-27|Monday]]
	![[dailyNotes/2022-03-27#^memo-link]]
- [[dailyNotes/2022-03-28|Tuesday]]
	![[dailyNotes/2022-03-28#^memo-link]]
- [[dailyNotes/2022-03-29|Wednesday]]
	![[dailyNotes/2022-03-29#^memo-link]]
- [[dailyNotes/2022-03-30|Thursday]]
	![[dailyNotes/2022-03-30#^memo-link]]
- [[dailyNotes/2022-03-31|Friday]]
	![[dailyNotes/2022-03-31#^memo-link]]
- [[dailyNotes/2022-04-01|Saturday]]
	![[dailyNotes/2022-04-01#^memo-link]]
- [[dailyNotes/2022-04-02|Sunday]]
	![[dailyNotes/2022-04-02#^memo-link]]

### Overview
```dataviewjs
const DAILY_NOTES_PATH = "02 Personal/02.01 Periodic Notes/2022/Daily/03 March";
const DATASET_TEMPLATE = {
	label: "Default",
	backgroundColor: 'rgba(255, 99, 132, 0.2)',
	borderColor: 'rgba(255, 99, 132, 1)',
	borderWidth: 1,
	fill: true,
	tension: 0.2
}
const DAY_ATTRIBUTES = new Map([
	['panic', {
		label: 'Panic',
	}],
	['money-spent', {
		label : 'Money Spent (£)',
		backgroundColor: 'rgba(85, 174, 229, 0.2)',
		borderColor: 'rgba(85, 174, 229, 1)',
	}],
	['prayer', {
		label : 'Prayer',
		backgroundColor: 'rgba(255, 211, 101, 0.2)',
		borderColor: 'rgba(255, 211, 101, 1)',
	}],
	['weather', {
		label : 'Weather (°C)',
		backgroundColor: 'rgba(92, 197, 193, 0.2)',
		borderColor: 'rgba(92, 197, 193, 1)',
	}],
]);

const getDaysPages = () => {
	const startOfWeek = dv.date("2022-03-31").startOf('week'); 
	const getDayPage = dayNum => dv.page(`${DAILY_NOTES_PATH}/${startOfWeek.plus({ days : dayNum }).toISODate()}`);
	return Array.from({length : 7}, (c,i) => getDayPage(i) || 0)
};

const generateDatasets = (map, template) => {
	const newMap = new Map([...map.entries()]);
	const daysPages = getDaysPages();
	const applyDefault = (def, obj) => Object.assign({}, def, obj);
	const addDataChart = (key, obj) => ({...obj, data : daysPages.map(p => p[key])});
	for (let [key, props] of newMap.entries()) {
		newMap.set(key, applyDefault(template, addDataChart(key, props)));
	}
	return [...newMap.values()];
}

const chartData = {
	type: 'line',
	data: {
		labels: ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"],
		datasets: generateDatasets(DAY_ATTRIBUTES, DATASET_TEMPLATE),
	}
}

window.renderChart(chartData, this.container);
```

```dataview
TABLE WITHOUT ID
	link(file.name) as "Day",
	feeling AS "💭",
	panic AS "🌪️",
	working-on AS "✏️",
	money-spent AS "💸",
	martial-arts AS "🥋",
	weather AS "☀️",
	prayer AS "🕋"
FROM "02 Personal/02.01 Periodic Notes"
WHERE week = [[2022 Week 13]]
SORT file.name ASC
```

### Journal