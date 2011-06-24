Before using
------------
The KeyboardStringReader needs a reference to System.Windows.Forms in order to get the capslock and numlock states, so a reference will need to be added to the XNA project.

How to use
----------

KeyboardStringReader textReader = new KeyboardStringReader();
StringBuilder inputText = new StringBuilder();

protected override void Update(GameTime gameTime)
{
	KeyboardState keyboard = Keyboard.GetState();
	this.textReader.Process(keyboard, gameTime, this.inputText);
}