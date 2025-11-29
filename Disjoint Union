// DSU
vector<int> parent;
vector<int> rank;

int find(int a)
{
    if(a == parent[a])
        return a;
// Path Compression
    return parent[a] = find(parent[a]);
}

void Union(int a, int b)
{
    int parent_a = find(a);
    int parent_b = find(b);
    
    if(parent_a == parent_b)
        return;

// Union by rank
    if(rank[parent_a] > rank[parent_b])
        parent[parent_b] = parent_a;
        
    else if(rank[parent_b] > rank[parent_a])
        parent[parent_a] = parent_b;
    
    else {
        parent[parent_b] = parent_a;
        rank[parent_a]++;
    }
    
    
}
