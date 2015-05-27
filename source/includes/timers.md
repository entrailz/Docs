# Timers

## Creating a timer

Sometimes you come across a situation which only a timer can fix. Timers are great for delaying code, allowing it to be run later. The following sections will show you the various timer types, and how to use them properly.

## timer.Once

> Basic example of timer.Once

``` csharp
timer.Once(0.5f, () =>
{
    ConsoleSystem.Broadcast("chat.add", 0, string.Format("<color=orange>{0}:</color> {1}", "SERVER", "Hello world!), 1.0);
});
```

``` javascript
timer.Once(3, function() {
    rust.BroadcastChat("SERVER", "Hello world!");
}, this.Plugin);
```

``` lua
timer.Once(3, function()
    rust.BroadcastChat("SERVER", "Hello world!")
end, self.Plugin)
```

``` python
def my_callback_func():
    rust.BroadcastChat("SERVER", "Hello world!")
timer.Once(3, Action(my_callback_func), self.Plugin)
```

> Example of timer.Once with a table

``` csharp
We need a CSharp example here
```

``` javascript
We need a JavaScript example here
```

``` lua
local timersVariable = {}
timersVariable["Notice1"] = timer.Once(3, function()
    rust.BroadcastChat("SERVER", "This is the Notice 1 every 3 seconds")
end)
timersVariable["Notice2"] = timer.Once(10, function()
    rust.BroadcastChat("SERVER", "This is the Notice 2 every 10 seconds")
end, self.Plugin)
```

``` python
We need a Python example here
```

Executes the specified function once after the specified delay.

## timer.Repeat

> Basic example of timer.Repeat

``` csharp
We need a CSharp example here
```

``` javascript
timer.Repeat(10, 0, function() {
    rust.BroadcastChat("SERVER", "Hello world!");
}, this.Plugin);
```

``` lua
timer.Repeat(10, 0, function()
    rust.BroadcastChat("SERVER", "Hello world!")
end, self.Plugin)
```

``` python
def my_callback_func():
    rust.BroadcastChat("SERVER", "Hello world!")
timer.Repeat(10, 0, Action(my_callback_func), self.Plugin)
```

Executes the specified function every "delay" seconds. If "repeats" is specified, the function will only be called "repeats" times.

## timer.NextFrame

> Basic example of timer.NextFrame

``` csharp
We need a CSharp example here
```

``` javascript
We need a JavaScript example here
```

``` lua
We need a Lua example here
```

``` python
We need a Python example here
```

Executes the specified function at the next frame.

## Destroying a timer

> Basic example in Unload

``` csharp
We need a CSharp example here
```

``` javascript
if (timerVariable) {
    timerVariable.Destroy();
}
```

``` lua
if timerVariable then
    timerVariable:Destroy()
end
```

``` python
if timerVariable:
    timerVariable.Destroy()
```

> Example in Unload with a table

``` csharp
We need a CSharp example here
```

``` javascript
We need a JavaScript example here
```

``` lua
for key, value in pairs(timersVariable) do
    timersVariable[key]:Destroy()
end
```

``` python
We need a Python example here
```

If you need to stop a timer, you can do so by destroying the instance of the timer. When used correctly, timers are automatically destroyed when the plugin is reload or unloaded.
