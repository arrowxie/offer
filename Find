#include<iostream>
#include<vector>

using namespace std;
bool Find(vector<vector<int> > array,int target)
{

	vector<vector<int> >::size_type row = array.size();
	if(row==0)
		return false;
	vector<int>::size_type coloumn = array[0].size();
	int i=0,j=coloumn-1;
	while(i>=0 && i<row && j>=0 && j<coloumn)
	{
		if(array[i][j]==target)
			return true;
		else if(array[i][j]<target)
			i++;
		else
			j--;
	}
	return false;
}

vector<vector<int> > init()
{
	vector<vector<int> > vet;
	
	int bias = 6;
	for(int i=0;i<5;i++)//row
	{
		vector<int> temp;
		for(int j=0;j<6;j++)//coloumn
			temp.push_back(j+bias);
		bias++;
		vet.push_back(temp);
	}
	return vet;
	//cout<<vet.size()<<endl;//row
	//cout<<vet[0].size()<<endl;//coloumn
}
void print(vector<vector<int> > vet)
{
	for(int i=0;i<5;i++)
	{
		for(int j=0;j<6;j++)
			cout<<vet[i][j]<<" ";
		cout<<endl;
	}
}
int main()
{
	vector<vector<int> > vet = init();
	print(vet);
	cout<<Find(vet,10)<<endl;
	return 0;
}
