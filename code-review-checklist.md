# Code Review Checklist

## Security

Test | Notes | Meets Qualifications
---- | ----- | --------------------
Admin pages cannot be accessed by non-admins | n/a |
Access callbacks are functional and set up appropriately. | Assume each user role and ensure proper callbacks. |
Server side validation of input values. | Use `check_plain` for input values, and `filter_xss` for values containing HTML. |
Client side validation of input values. | This includes sanitization and encoding/decoding of potential breaking characters. |

## Error Logging and Handling

Test | Notes | Meets Qualifications
---- | ----- | --------------------
Get rid of all warnings, errors, and notices. | n/a |
Make sure there are no errors or warnings in the browser inspector console. | n/a |
Handle error conditions properly. | Example: If the form did not save correctly, display error messages to the user. |

## Browser Support

Test | Notes | Meets Qualifications
---- | ----- | --------------------
Chrome | |
Firefox | |
Edge | |
Safari | |
Internet Explorer | |

## Date / Time

Test | Notes | Meets Qualifications
---- | ----- | --------------------
All times are either ISO-8601 or unix timestamp. |
Ensure timezones are handled correctly. |
