# Put the computer to work

{% tabs %}
{% tab title="Prompt" %}
{% hint style="info" %}
Can you write a loop that runs almost forever?
{% endhint %}

{% hint style="warning" %}
**Challenge**

Can you write it so that the computer shows you how hard it's working?
{% endhint %}

{% hint style="danger" %}
When your Python program runs for a long time, you can cancel it with `ctl-c` on Windows, and `cmd-c` on Mac.
{% endhint %}
{% endtab %}

{% tab title="Solution: Long loop" %}
```python
for i in range(1000000 * 100000):
    print('Working hard! Press ctl-c or cmd-c to stop me :)')
```
{% endtab %}

{% tab title="Solution: How much work is done?" %}
```python
for i in range(100000 * 100000):
    print(i)
```
{% endtab %}
{% endtabs %}



