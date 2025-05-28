#include <bits/stdc++.h>
using namespace std;

struct node {
    int data;
    node* link;
};

void add_at_end(node* head, int data) {
    node* ptr = head;
    node* temp = new node;

    temp->data = data;
    temp->link = nullptr;

    while (ptr->link != nullptr) {
        ptr = ptr->link;
    }
    ptr->link = temp;
}

int main() {
    node* head = new node;
    head->data = 45;
    head->link = nullptr;

    add_at_end(head, 67);

    node* ptr = head;
    while (ptr != nullptr) {
        cout << ptr->data << " ";
        ptr = ptr->link;
    }

    return 0;
}
