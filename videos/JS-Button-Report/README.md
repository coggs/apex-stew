[Oracle APEX Javascript Button on Report Row](https://youtu.be/gkpD8wE5HWc)

Add a Javascript Button onto a Report and use it to update the row

Here is the code that was pasted into the Application

```
<button class="offloadButton
           t-Button
           t-Button--simple
           t-Button--hot
           t-Button--stretch" data-loan-id="#ID#" type="button">
    <span class="t-Button-label">RETURNED</span>
</button>

confirm($(this.triggeringElement).data('loan-id'));

$s('LOAN_UPDATE_ID', $(this.triggeringElement).data('loan-id'));

UPDATE LOAN SET RETURNED_WORKING='Y' WHERE ID = :LOAN_UPDATE_ID;
```
