# Number Management

The DNRC areas, DNRC units and activity roles that are available
to be associated with financial codes can change on a yearly basis.
Users with the `OWNER` application role can modify these attributes for
the current and upcoming year. These settings are available in the
configuration page, which can be navigated to by using the `Configuration`
link in the navigation header.

## Managing DNRC Areas and Units

Areas and units are managed using identical interfaces.

### Adding Areas or Units

To add an area or unit, find the appropriate list and click on the `Add`
button underneath the list's title. Two input fields will appear to enter
the new item's name and three letter abbreviation. After entering the
information, it is possible to add the item for use in the current year, or
use in the next year by using the `Add` or `Add for next year` buttons.

If the new item is added successfully, then the new item will be displayed
at the top of the list. Otherwise, an error message will appear. Item's names
and abbreviations must be unique within their group.

### Disabling Areas or Units

To disable an item, find it in the appropriate list. Underneath the item's
general information, there are two checkboxes. If the
`Disabled for current year` checkbox is checked, the item will not be available
for use in the current year. If the `Disabled for next year` box is checked, then
the item will not be activated for next year or any year after that.

## Managing Activity Roles

### Number Templates

Number templates are used to specify how the numbers associated with
an activity role are generated. Each template is a series of
placeholder characters that determine what the character in the same
place of the generated numbered will be. These placeholders can be
resolved to the character itself, a digit of the current year, or a
digit from the activity role's counter. Use the table below to
see which characters in a template are tranformed when a number is
generated:

| Character | Description |
|-----------|-------------|
| X         | Replaced by a digit from the activity role's counter |
| O         | Replaced by a digit from the activity role's counter if there aren't enough `X` placeholders |
| Y         | Replaced by a digit from the code's year |

Characters are replaced right-to-left starting with the counter's or year's least
significant digit. Any placeholder that doesn't have a digit assigned
to it will be set to `0`. For example, for the template `XXX`, with a
counter value of `25`, the generated value is `025`.

Placeholders do not need to be contigous. For example, for the
template `X1X` with a counter value of `36`, the generated value will
be `316`.

For the placeholders `X` and `O`, if there are too many digits in the
counter to encode, no result will be produced.

For the placeholder `Y`, the year is truncated to match the number of
`Y` placeholders given. For example, with the template `YY`, and the
year 2021, the generated value will be `21`.

#### The `O` Placeholder

Unlike the `X` placeholder, the `O` placeholder doesn't directly
place it's digits into the generated string. Instead, the digits are
transformed into a base 27 number which is encoded using the
digits `0`, `a`, `b`, `c`, `d`, ... `z`. This number is then placed
into the template as usual.

For example, if the template `O` needed to encode the number `11`, it
would use the character `k`, as it is the 11th letter of the
alphabet. As another example, the template `OO` encodes the number 28
as `a0` and the number 30 as `ac`.
