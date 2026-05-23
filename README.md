*API translation to GDJS(gdevelop JavaScript)*


  print: (v) => print(v),
  variables: (v) => hhj(v),
  log: (...args) => console.log(args),
  getBlockInSight: () => runtimeScene._blockInSight,
  getWorld: () => world,
  disableBlockPlacement: (b) => runtimeScene.getVariables().get("forbidPlacement").setBoolean(b),
  player: () => runtimeScene.getObjects("body")[0],
  keyPressed: (k) => runtimeScene.getGame().getInputManager().isKeyPressed(k),
  onKeyPressed: (k) => runtimeScene.getGame().getInputManager().onKeyPressed(k),
  anyKeyReleaseed: (k) => runtimeScene.getGame().getInputManager().anyKeyReleased(),
  onMouseClicked: (k) => runtimeScene.getGame().getInputManager().onMouseButtonPressed(k),
  isMouseClicked: (k) => runtimeScene.getGame().getInputManager().isMouseButtonPressed(k),
  posToChunkPos: (x, y) => posToChunkPos(x, y),
  updateChunk: (k) => updateChunk(k),
  getChatInput: () => getInputChatTxt(),
  setChatInput: (v) => setInputChatTxt(v),
  GLTFloader: () => new THREE_ADDONS.GLTFLoader(),
  raycaster: () => new THREE.Raycaster(),
  camera: () => runtimeScene.getLayer("").getRenderer().getThreeCamera(),
  scene3D: () => runtimeScene.getLayer("").getRenderer().getThreeScene(),//to add 3d objects
  getPath: () => getPath(),
  getPathDelimiter: () => gdjs.fileSystem.getPathDelimiter()
