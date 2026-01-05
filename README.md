#include <iostream>
using namespace std;

int main() {
    
    const int N = 2;
    int matrixA[2][2] = {{2, 3},{5, 6}};
    for(int i=0;i<2;i++)
    {
        for(int j=0;j<2;j++)
        {
          cout<<matrixA[i][j]<<" ";
        }
        cout<<endl;
    }
    cout<<endl;
    int matrixB[N][N] = {{9,8},{6, 5}};
    for(int i=0;i<2;i++)
    {
        for(int j=0;j<2;j++)
        {
          cout<<matrixB[i][j]<<" ";
        }
        cout<<endl;
    }
        int result[N][N];
        for (int i = 0; i < N; i++) 
    {
           for (int j = 0; j < N; j++)
        {
        result[i][j] = 0; 
            for (int k = 0; k < N; k++)
            {
        result[i][j] += matrixA[i][k] * matrixB[k][j];
            }
        }
    }
        cout << "Resulting Matrix:" << endl;
    for (int i = 0; i < N; i++) {
        for (int j = 0; j < N; j++) {
            cout << result[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}
