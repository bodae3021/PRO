# PRO
PROGRAMMER
#include<iostream>
#include<conio.h>
#include <string>
using namespace std;
struct node{
	string name;
	long id;
	int study_year;
	double grade;
	string mail;
	long phone;
	node *next;
	node *prev;
	node(){
		next=NULL;
		prev=NULL;
	}
	
};
struct list{
	node *head;
	list(){
		head=NULL;
	}
	bool empty() {
		if(head==NULL) 
		 return true;
		else
		   return false;
	}
	void insert() {
		node *newnode=new node();
		cout<<"enter student name"<<endl;
		cin>>newnode->name;
		cout<<"enter student id"<<endl;
		cin>>newnode->id;
		cout<<"enter student mail"<<endl;
		cin>>newnode->mail;
		cout<<"enter student year"<<endl;
		cin>>newnode->study_year;
		cout<<"enter student grade"<<endl;
		cin>>newnode->grade;
		cout<<"enter student phone num"<<endl;
		cin>>newnode->phone;
		if(empty()) {
			newnode->next=NULL;
			head->prev=newnode;
			head=newnode;
			
			
		}
		else{
			newnode->next=head;
			head->prev=newnode;
			head=newnode;
		}
	}
	void last(){
		node *last=head;
		node *newnode=new node();
		cout<<"enter student name"<<endl;
		cin>>newnode->name;
		cout<<"enter student id"<<endl;
		cin>>newnode->id;
		cout<<"enter student mail"<<endl;
		cin>>newnode->mail;
		cout<<"enter student year"<<endl;
		cin>>newnode->study_year;
		cout<<"enter student grade"<<endl;
		cin>>newnode->grade;
		cout<<"enter student phone num"<<endl;
		cin>>newnode->phone;
		while(last!=NULL) {
			last=last->next;
		}
		last->next=newnode;
		newnode->prev=last;
		last=newnode;
		
		
	}
	void print() {
		node *temp=head;
		while(temp!=NULL) {
			cout<<temp->name<<endl;
			cout<<temp->grade<<endl;
			cout<<temp->mail<<endl;
			temp=temp->next;
		}
	}
};
int main() {
	list y;
	while(true) {
	
	cout<<"1-inseart first"<<endl;
	cout<<"2-inseart lA"<<endl;
	cout<<"3-print"<<endl;
	int c;
	cin>>c;
	switch(c) {
		case 1:
			y.insert();
		break;
		case 2:
			y.last();
		break;
		case 3 :
			y.print();
		break;
		default:
			cout<<"wrom=ng";
		break;
		
	}
}
}

