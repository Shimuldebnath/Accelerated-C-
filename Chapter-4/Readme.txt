Chapter 4: Organizing programs and data

vector<double> homework;
vector<double>& hw = homework;
// hw is a synonym for homework
const vector<double>& cp= homework;
// cp is a reference to homework and it is not possible to edit cp as it is const.

Header files should be guarded against multiple inclusion by wrapping the file in an
#ifndef GUARD _header_name directive. Headers should avoid declaring names that they
do not use. In particular, they should not include using -declarations, but instead should
prefix standard-library names with std:: explicitly.

