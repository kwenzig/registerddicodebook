__How to read:__ 
- The following text is based on the form available at https://www.iana.org/form/media-types. When rendered on GitHub, the suggested entries are displayed in a light grey highlighted box with a copy icon on the right. In the Markdown source, these sections are enclosed in triple backticks (` ``` `) and indicate the exact text to be entered into the form; any placeholders should be replaced as appropriate. 
- All other text reproduces the structure of the original form and serves explanatory purposes only. 
- Where a selection from predefined options is required, the full list of available options - along with brief descriptions - is provided below.

# Application for a Media Type

We recommend that you read the following RFCs before proceeding with this application. It is important that you understand the application process and requirements completely. These documents are the standards for media types:

 - [RFC 2045](https://www.iana.org/go/rfc2045) - MIME formats and encodings 
 - [RFC 2046](https://www.iana.org/go/rfc2046) - Definition of media types 
 - [RFC 2077](https://www.iana.org/go/rfc2077) - Model top-level media type 
 - [RFC 6657](https://www.iana.org/go/rfc6657) - Update to MIME regarding "charset" parameter handling in textual media types 
 - [RFC 7303](https://www.iana.org/go/rfc7303) - XML media types 
 - [RFC 8081](https://www.iana.org/go/rfc8081) - Font top-level media type 
 - [RFC 9695](https://www.iana.org/go/rfc9695) - Haptics top-level media type 
 - [RFC 9694](https://www.iana.org/go/rfc9694) - Guidelines for the definition of new top-level media types 
 - [RFC 6838](https://www.iana.org/go/rfc6838) - Media type specifications and registration procedures 

#### Your Full Name

```
Name
```

#### Your E-mail

```
E-mail
```

Please read the following questions carefully and provide complete answers. Write "N/A" for fields that are not applicable.

When referring to specifications, please provide URLs (if applicable).

#### Type Name

What is the media type name?

```
Selection Option: application, text etc.
```

Options:
 - application (RFC 2046)
 - audio (RFC 2046)
 - font (RFC 8081)
 - haptics (RFC 9695)
 - image (RFC 2046)
 - message (RFC 2046)
 - model (RFC 2077)
 - multipart (RFC 2046)
 - text (RFC 2046)
 - video (RFC 2046)

See the [Top-Level Media Types](https://www.iana.org/assignments/top-level-media-types) registry.

#### Subtype Name

What is the media subtype name? (The prefix, if any, will be taken from the drop-down menu and should be omitted from the text field.)

```
Selection Option: vnd/no/prs
```

Options:
- Vendor Tree (vnd. prefix)
- Standards Tree (no prefix)
- Personal Tree (prs. prefix)

```
Name
```

Review the [existing subtype names](https://www.iana.org/assignments/media-types). See also [RFC 2046](https://www.iana.org/go/rfc2046) and [RFC 6838](https://www.iana.org/go/rfc6838) (sections 3 and 4.2).

Registrations in the standards tree must be approved by the IESG or correspond to a formal publication by a recognized standards body. See [RFC 6838](https://www.iana.org/go/rfc6838) (section 3.1).

If the name includes a suffix (text that follows a "+" at the end of the subtype name), that suffix must be listed in the [Structured Syntax Suffixes](https://www.iana.org/assignments/media-type-structured-suffix) registry.

The appearance of a dot (".") in a standards-tree subtype name would require registration of a new facet, which may not be what is intended.

#### Required Parameters

Describe the required parameters. (If none, enter "N/A.")

```
Parameter
```

See [RFC 2046](https://www.iana.org/go/rfc2046), section 1, and [RFC 6838](https://www.iana.org/go/rfc6838), section 4.3.

Text types should pay attention to the discussion of the charset parameter in [RFC 6838](https://www.iana.org/go/rfc6838), section 4.2.1.

#### Optional Parameters

Describe the optional parameters. (If none, enter "N/A.")

```
Parameter
```

See [RFC 2046](https://www.iana.org/go/rfc2046), section 1, and [RFC 6838](https://www.iana.org/go/rfc6838), section 4.3.

#### Encoding Considerations

```
Select option: 7-/8-bit/binary/framed
```

Options:
- 7-bit text
- 8-bit text (this media type may require encoding on transports not capable of handling 8-bit text)
- binary (this media type may require encoding on transports not capable of handling binary)
- framed (transport must provide framing information)

_Additional notes (optional):_

```
Note
```

See [RFC 2045](https://www.iana.org/go/rfc2045), section 6, and [RFC 6838](https://www.iana.org/go/rfc6838), section 4.8.

8-bit data consists of lines no longer than 998 octets, separated by CRLF.

The following questions should help determine whether to select "8-bit" or "binary":

1. Can NUL octet appear in the format? If yes, then encoding is "binary."
2. Can CR and/or LF octets appear outside of CRLF sequence? If yes, then encoding is "binary."
3. Does the format allow for lines longer than 998 octets? If yes, then encoding is "binary."
4. Otherwise the encoding is "8-bit."

If the format is based on JSON or XML, "binary" should generally be selected due to the possibility that lines could be longer than 998 octets.

If the format is encoded using UTF-16, the encoding is always "binary."

#### Security Considerations

Provide a discussion of the security considerations.

```
Consideration
```

All media type registrations must describe their security considerations; simply saying there are none or leaving the section blank is unacceptable.

In discussing the security considerations for a media type, it is necessary to cover at least these points:

1. State whether or not the media type contains active or executable content. If the media type does contain executable content, explain what measures have been taken to insure that it can be executed safely, e.g. a sandbox, safe operation set, signed content, etc.
2. State whether or not the information contained in the media type needs privacy or integrity services.
3. If the answer to (2) is yes, elaborate on any privacy or integrity services the media type itself provides. If it doesn't provide such services, explain how they should be provided externally, e.g., through the use of SSL/TLS.
4. If the media type uses an existing format, e.g. XML or JSON, the security considerations for that format must be referenced and any issues specific to the usage of that format, e.g., XML extensibility, must be described.
   - (4a) If the media type employs compression, the security considerations associated with that usage must be covered.
   - (4b) If the media type employs a container format, e.g., ZIP, any issues associated with that usage need to be described.
5. If the media type incorporates links that must be referenced in order to properly interpret the type, this should be noted.

Finally, although it is discouraged, it is acceptable to simply say that the security considerations of the media type have not been assessed.

See [RFC 6838](https://www.iana.org/go/rfc6838), section 4.6.

#### Interoperability Considerations

Provide a discussion of the interoperability considerations.

```
Consideration
```

See [RFC 6838](https://www.iana.org/go/rfc6838), section 4.5.

#### Published specification

Provide references to the published specification.

```
Specification
```

See [RFC 6838](https://www.iana.org/go/rfc6838), section 4.10.

#### Application Usage

Describe applications which use/will use this media type.

```
Applications
```

See [RFC 6838](https://www.iana.org/go/rfc6838), section 4.5.

#### Fragment Identifier Considerations

```
Consideration
```

See [RFC 6838](https://www.iana.org/go/rfc6838), section 4.11.

#### Restrictions on Usage

```
Restriction
```

See [RFC 6838](https://www.iana.org/go/rfc6838), section 4.9.

#### Provisional Registrations

Is this a request for provisional registration only? (Vendor-tree and personal-tree requests must select "No.")

```
Select option: Yes/No
```

Options:
- Yes. This is a request for provisional standards-tree registration only. A request for permanent registration will be submitted at a later date.
- No. This is a request for vendor-tree, personal-tree, or permanent standards-tree registration.

See [RFC 6838](https://www.iana.org/go/rfc6838), section 5.2.1 and the [provisional standards-tree media type registry](https://www.iana.org/assignments/provisional-standard-media-types).

#### Additional Information

See [RFC 6838](https://www.iana.org/go/rfc6838), section 4.12.

_Deprecated alias names for this type_

```
Alias
```

_Magic number(s)_

```
Number
```

_File extension(s)_

```
Extension
```

_Macintosh File Type Code(s)_

```
Code
```

_Object Identifier(s) or OID(s) — See [RFC 1494](https://www.iana.org/go/rfc1494)._

```
Identifiers
```

#### Intended Usage

```
Select Option: COMMON/LIMITED/OBSOLETE
```

Options:
- COMMON
- LIMITED USE
- OBSOLETE

_Additional information (if necessary):_

```
Information
```

"LIMITED USE" can be appropriate when the media type is restricted in its usage, such as when it is used only in a particular protocol (e.g. HTTP, but not email) or application, and its use is not recommended in other contexts.

#### Other Information & Comments

```
Other
```

#### Contact Person

See [RFC 6838](https://www.iana.org/go/rfc6838), section 5.5.

_Contact Name_

```
Name
```


_Contact Email Address_

```
dditcmgr@gmail.com
```

_Author/Change Controller (for standards-tree registrations, this is typically the standards body)_

```
DDI Alliance, https://ddialliance.org/
```

By submitting my personal data, I agree that my personal data will be processed in accordance with our [Privacy Policy](https://www.icann.org/privacy/policy) and agree to abide by the website [Terms of Service](https://www.icann.org/privacy/tos).
