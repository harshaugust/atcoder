//
// Created by Harsh Kumar on 29/05/24.
//
#include <vector>
#include <iterator>
#include <algorithm>
#include <queue>
#include <iostream>
#include <stack>
#include <set>
#include <unordered_set>
#include <map>
#include <queue>
#include <cstdio>
#include <numeric>
#include <cmath>
#include <deque>
#include <unordered_set>
#include <iomanip>
#include <cmath>
#include <fstream>
#include <string>
#include <iostream>
#include <unordered_map>
using namespace std;
#define int long long
#define vi vector<int>
#define all(x) x.begin(), x.end()
#define rep(i, n) for (int i = 0; i < n; i++)
const int mxn = 2e5 + 5;
const int mod = 1e9 + 7;

void solve() {
  int n;
  cin >> n;
  vector<pair<int, int>> v;
  set<pair<int, int>> f, s;
  map<pair<int, int>, int> pos;
  for (int i = 0; i < n; i++) {
    int x, y;
    cin >> x >> y;
    v.push_back({x, y});
    pos[{x, y}] = i;
    s.insert({y, x});
  }
  sort(all(v));
  reverse(all(v));
  for (int i = 0; i < n; i++) {
    int first = v[i].first;
    int second = v[i].second;
    pair<int, int> temp = {second, first};
    if (s.count(temp) == 0) continue;
    else {
      f.insert(v[i]);
      s.erase(temp);
      auto it = s.lower_bound(temp);
      it;
      s.erase(it, s.end());
    }
  }
  cout << f.size()  + s.size() << endl;
  vector<int> res;
  for (auto x : f) {
    res.push_back(pos[x] + 1);
  }
  for (auto [x, y] : s) {
    res.push_back(pos[{y, x}] + 1);
  }
  sort(all(res));
  for (auto x : res) {
    cout << x << " ";
  }
  cout << endl;
}

signed main() {
  ios_base::sync_with_stdio(false);
  cin.tie(NULL);

#ifndef ONLINE_JUDGE
    freopen("input.txt", "r", stdin);
    freopen("output.txt", "w", stdout);
#endif
  int t;
//  cin >> t;
  t = 1;
  for (int i = 1; i <= t; i++) {
    solve();
  }
}
// https://atcoder.jp/contests/abc392/tasks/abc392_c
