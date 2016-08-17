
## Installation

The package can be installed via NPM:

```
npm install react-datepicker-oev --save

## log
version 1.0.5 : change logic to date range input
version 1.0.4 : remove trigle in date range picker
version 1.0.3 : add quick options for ranges
version 1.0.2 : change package.json
version 1.0.1 : fix bug config module
version 1.0.0 : init

*********************************************************************************************
for quick option day:

let datepickerQuickOptions = [{
			"label": "One month ago",
			"value": {"type": "month", "change": -1}
		}, {
			"label": "Half year ago",
			"value": {"type": "month", "change": -6}
		}, {
			"label": "One year ago",
			"value": {"type": "year", "change": -1}
		}];

<DatePicker selected={startDate}
            selected2={endDate}
            onChange={handleStartDateChange}
            onChange2={handleEndDateChange}
            placeholderText = "Select Date"
            dateFormat="YYYY/MM/DD"
            showYearDropdown
            minDate={maxDate}
            isDateRangePicker={true}
            quickOptionsRanges={quickOptionRanges}
            fixedHeight={true}
/>

---------------------------------------------------------------------------------------------

for quick option ranges:

let quickOptionRanges = [{
            "label": "Next 1 week",
            "value": {"type": "week", "change": 2}
        }, {
            "label": "Next 1 month",
            "value": {"type": "month", "change": 1}
        }, {
            "label": "Next 3 months",
            "value": {"type": "month", "change": 3}
        }, {
            "label": "Next 6 months",
            "value": {"type": "month", "change": 6}
        }, {
            "label": "Last week",
            "value": {"type": "week", "change": -2}
        }, {
            "label": "Last month",
            "value": {"type": "month", "change": -1}
        }, {
            "label": "Last 6 months",
            "value": {"type": "month", "change": -6}
        }];

<DatePicker selected={startDate}
            selected2={endDate}
            placeholderText = "Select Date"
            dateFormat="YYYY/MM/DD"
            showYearDropdown
            maxDate={maxDate}
            isDateRangePicker={true}
            quickOptionsRanges={quickOptionRanges}
            fixedHeight={true}
            popoverAttachment='top right'
            popoverTargetAttachment='bottom right'
            onApply={handleChangeDatePicker}
/>