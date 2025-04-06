# blind-6-75
Maximum product subarray
 Maximum product subarray



extreme positive variable - we try to store extreme positive contiguous subarray product value from beginning/last zero encountered to current index.

( it may not be positive ,if elements seen so far are negative. i.e to the best of ability ,we try to store extreme positive subarray product value)



extreme negative variable - we try to store extreme negative contiguous subarray product value from beginning/last zero encountered to current index.

( it may not be negative ,if elements seen so far are positive. i.e to the best of ability ,we try to store extreme negative subarray product value)



and then there is a result variable ,used to store the maximum product subarray.

In the beginning all are initialized to first element of the list.

Iterate once through rest of the list.

As we go along use temp_extreme_positive variable to handle circular updation dependency b/w extreme_positive and extreme_negative variable. i.e updating one irritates other . 

so using temporary variable to update extreme_positive without modifying extreme_positive.

update result at each index.

then update extreme_negative.

now equate extreme_positive to temp_extrem_positive.( bcoz updation of extreme_positve wouldn't have been possible ,bcoz extreme_negative changed in previous step).
