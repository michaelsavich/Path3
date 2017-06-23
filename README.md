# Path3
A simple class for drawing 3D paths using SceneKit

## Example usage:

    let scene: SCNScene = sceneCreatedEarlier
    var points: [SCNVector3] = arrayOfPointsFromEarlier

    let path = Path3()

    var nodes: [SCNNode] = []
    for point in points {
        nodes.append(path.continuePath(from: point)!)
    }

    for node in nodes { scene.rootNode.addChildNode(node) }
