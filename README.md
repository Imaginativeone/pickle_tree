

# Pickle Tree

> Pickle tree is a tree component written as completely pure javascript. Just send json file on object create and have fun :-D 

> Pickle tree does't need anything except you !

**Badges Falan**

- Simple javascript ability
- Simple css ability for some style editing for your project




## Initiation And Using Example 

> Initiate like this :

```javascript


const tree = new PickleTree({
        c_target: 'div_tree',
        rowCreateCallback: (node) => {
            //console.log(node)
        },
        switchCallback: (node) => {
            //console.log(node)
        },
        drawCallback: () => {
            //console.log('tree drawed ..');
        },
        c_config: {
            foldedStatus: false,
            logMode: false,
            switchMode: true,
            familyMode: true
        },
        c_data: [{
            n_id: 1,
            n_title: 'falan1',
            n_parentid: 0,
            n_checked: true
        }, {
            n_id: 2,
            n_title: 'falan2',
            n_parentid: 0
        }, {
            n_id: 3,
            n_title: 'falan3',
            n_parentid: 0
        }, {
            n_id: 4,
            n_title: 'falan1-1',
            n_parentid: 1
        }, {
            n_id: 5,
            n_title: 'falan1-2',
            n_parentid: 1
        }, {
            n_id: 10,
            n_title: 'falan1-2-1',
            n_parentid: 5
        }]
    });
```

---

> After that you can use some addional events for node like those:

```javascript

    //for getting node from its id :
    let our_node = tree.getNode('5');

    //for deleting node
    our_node.deleteNode();

    //for toggling
    our_node.toggleNode();

    //for getting its childs
    our_node.getChilds();

    //for check / uncheck node
    our_node.toggleCheck(true / false);


    // for creating new  node manualy
    let new_node = tree.createNode({
        n_value: 5,
        n_title: 'falan gibi 5',
        n_id: 5,
        n_elements: [],
        n_parent: tree.getNode(4),
        n_checkStatus: false
    });

```

---

## Installation

- Just include js and css file to your project then you can use it

### Clone

- Clone this repo to your local machine using `https://github.com/freakazoid41/pickletree`

