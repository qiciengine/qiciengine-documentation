# [qc.Node](CNode.md).find

## Prototype
* [qc.Node](CNode.md) find(string path)

## Paramters
| Paramter | Type |  Description |
| --------- | --------- | --------- |
| path | string |  The node's name. If path contains a '/' character it will traverse the hierarchy like a path name. |

## Description
Finds a game object by name and returns it.

## Sample
````
    node.find('uiLogin/loginBtn/text');
````
