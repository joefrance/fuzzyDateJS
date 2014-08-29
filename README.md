fuzzyDateJS
===========

Framework for fuzzy dates in JavaScript.

Thanks to Lee Brandt - @leebrandt - for listening to my idea for fuzzy dates after devLink 2014.

New type to be called:

  fuzzyDate (perhaps "inherited from JavaScript Date)
  
Will start with:

  http://code.tutsplus.com/tutorials/build-your-first-javascript-library--net-26796
  http://www.w3schools.com/jsref/jsref_obj_date.asp
  https://github.com/philbooth/vagueTime.js
  
The abstract is that:

1. Create "class" structure to allow date storage like:
  a. In the 15th century
  b. Yesterday (need anchor metadata for context)
  c. Last week
  d. About 1850
  e. In the early 1700s
  f. In the second year of Darius the king, in the sixth month, on the first day of the month
  g. In the first year of Darius the son of Ahasuerus
  h. Next year
2. The data type would need at least the following:
  a. STRING to contain the description of the "fuzzy date"
  b. MinDateTime
  c. MaxDateTime
  d. Possible language indicator
  e. "Enum" quality indicator:
    i. Exact date
    ii. Approximate date
    iii. Year-exact-month-unknown
    iv. Year-fuzzy-month-exact-day-fuzzy
3. Possible integration with:
  a. MomentJS
  b. valueTime.js
4. Functions to include:
  a. Date math between:
    i. JavaScript Date Object (JSDate) and fuzzyDate:
      1. Yields new fuzzyDate if fuzzyDate is other than "Exact Date"
      2. Yields new Date Object if fuzzyDate is "Exact Date"
    ii. fuzzyDate and fuzzyDate:
      1. Yields new fuzzyDate if EITHER fuzzyDates is other than "Exact Date"
      2. Yields new Date Object if BOTH fuzzyDates are "Exact Date"

More work needed.
