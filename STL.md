    //-------------------------------------Pair-------------------------------------

    pair<int, int> b = {1,3};
    cout << b.first << " " << b.second<<endl;

    pair <int , pair <int , int>> p = { 1 , { 3 , 4 }};
    cout << p.first << " " << p.second.first << " " << p.second.second<<endl;

    pair <int , int> arr[] = {{1,2} , {3,4} , {5,6} ,{7,8}};
    cout<< arr[1].second<<endl;

    // output:-
    // 1 3
    // 1 3 4
    // 4

    //---------------------------------vector------------------------------------------

    vector<int> v;
    v.push_back(1);
    cout<<v[0]<<endl; //output: 1

    v.emplace_back(2);
    cout<<v[0]<<" "<<v[1]<<endl; //output: 1 2

    vector<pair<int,int>> vec;
    vec.push_back({1,2});
    vec.emplace_back(3,4);

    cout<<vec[0].first<<" "<<vec[0].second<<" "<<vec[1].first<<" "<<vec[1].second<<endl;
    //output: 1 2 3 4

    vector<int> vi (5,12) ; // vector of length 5 all elements 12
    // vecotr<int> vi (5); // vector of length 5 all elements 0 or garbage depending on compiler

    for(int i = 0; i < 5; i++ ) cout<< vi[i] <<" ";// output: 12 12 12 12 12
    cout<<endl;

    vector<int> v2(vi); // passing the value of vi to v2
    for(int i = 0; i < 5; i++ ) cout<< v2[i] <<" ";// output: 12 12 12 12 12
    cout<<endl;


    //____________iterator__________
    // iterator is basicall a pointer in c++
    v = {10,20,30,40,50};
    vector<int>::iterator it = v.begin();
    cout << *(it) <<endl; // opt:- 1
    it +=2;
    cout << *(it) <<endl; // opt:- 3

    // here are some iterators
    // v.end()
    // v.begin()
    // v.back() points to the last element of the array
    // v.rend()   reverse end 
    // v.rbegin()  reverse begin if we add 1 then it moves backward from 50 to 40 to 30 ...
    // these points to 
    //   
    //                              back
    //                               |
    //        { 10 , 20 , 30 , 40 , 50 }    
    //     ^    ^                   ^    ^
    //     |    |                   |    |
    //   rend  begin            rbegin   end
    // 
    // 
