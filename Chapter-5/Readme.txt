Chapter 5: Using sequential containers and analyzing strings

Iterator is of two types:
container-type::const_iterator
container-type::iterator

Spliting a string using vector:
#include <iostream>
#include <string>
#include <vector>
#include <cctype>


std::vector<std::string> split(const std::string& s)
{
    std::vector<std::string> ret;
    typedef std::string::size_type string_size;
    string_size i = 0;
    while(i != s.size()) {
        while(i != s.size() && isspace(s[i])) {
            i++;
        }
        string_size j = i;
        while(j != s.size() && !isspace(s[j])) {
            j++;
        }
        if( i != j) {
            ret.push_back(s.substr(i,j-i));
            i = j;
        }
    }
    return ret;
}

int main()
{
    std::vector<std::string> vec;
    std::string str;
    std::cout << "Enter a string:";
    getline(std::cin,str);
    vec = split(str);
    std::vector<std::string>::const_iterator iter;
    for(iter = vec.begin();iter!=vec.end();iter++) {
        std::cout << *iter << std::endl;
    }
    return 0;
}


