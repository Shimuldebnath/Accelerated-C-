Chapter 4: Organizing programs and data

vector<double> homework;
vector<double>& hw = homework;
// hw is a synonym for homework
const vector<double>& cp= homework;
// cp is a reference to homework and it is not possible to edit cp as it is const.

