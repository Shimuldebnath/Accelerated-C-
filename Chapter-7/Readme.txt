Chapter 7: Associative containers

Associative data structure: stores key value pair
Associative array: In c++ part of library, Most common is called map
One fundamental difference between map and vector:
Index of vector need not be an integer.
Map:
int main() {
    string s;
    map<string, int> counters;
    for (int i = 0; i < 5; i++)
    {
        cin>>s;
        counters[s]++;
    }


    for(map<string,int>::const_iterator it = counters.begin();it!=counters.end();it++)
    {
        cout<<it->first<<"\t"<<it->second<<endl;
    }

    return 0;
}

The pair associated with a map has a key type that is const. 

