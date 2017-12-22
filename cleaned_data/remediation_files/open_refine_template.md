# OpenRefine Template for CDF (migration)

---

## Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```

## Row Template

```
<mods>
<identifier type="local">{{cells["adminDB"].value}}</identifier>
<identifier type="pid">{{cells["pid"].value}}</identifier>
{{if(isBlank(cells["identifier_isbn"].value),'', '<identifier type="isbn">' + cells['identifier_isbn'].value + '</identifier>') +
if(isBlank(cells["identifier_issn"].value),'', '<identifier type="issn">' + cells['identifier_issn'].value + '</identifier>')}}
{{'<titleInfo><title>' + cells['title'].value + '</title></titleInfo>'}}
{{if(isBlank(cells['abstract'].value), '', '<abstract>' + cells['abstract'].value + '</abstract>')}}
{{'<originInfo>' + if(isBlank(cells['date_text'].value), '', '<dateIssued>' + cells['date_text'].value + '</dateIssued>') + if(isBlank(cells['date_single_start'].value), '', '<dateIssued encoding="edtf" point="start" keyDate="yes">' + cells['date_single_start'].value + '</dateIssued>') + if(isBlank(cells['publisher'].value), '', '<publisher>' + cells['publisher'].value + '</publisher>') + '</originInfo>'}}
{{'<physicalDescription' + if(isBlank(cells['extent'].value), '', '<extent>' + cells['extent'].value + '</extent>') + if(isBlank(cells['form'].value), '', '<form' + if(isBlank(cells['form_URI'].value), '>', ' authority="' + cells['form_URI'].value + '>') + cells['form'].value + '</form>') + '<digitalOrigin>reformatted digital</digitalOrigin></physicalDescription>'}}
{{if(isBlank(cells['name'].value), '', '<name'+ if(isBlank(cells['name_URI'].value), '', ' valueURI="' + cells['name_URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name'].value + '</namePart>' + if(isBlank(cells['name_role'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name_role_URI'].value + '">' + cells['name_role'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['name_2'].value), '', '<name'+ if(isBlank(cells['name_URI_2'].value), '', ' valueURI="' + cells['name_URI_2'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_2'].value + '</namePart>' + if(isBlank(cells['name_role_2'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name_role_URI_2'].value + '">' + cells['name_role_2'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['name_3'].value), '', '<name'+ if(isBlank(cells['name_URI_3'].value), '', ' valueURI="' + cells['name_URI_3'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_3'].value + '</namePart>' + if(isBlank(cells['name_role_3'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name_role_URI_3'].value + '">' + cells['name_role_3'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['name_4'].value), '', '<name'+ if(isBlank(cells['name_URI_4'].value), '', ' valueURI="' + cells['name_URI_4'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_4'].value + '</namePart>' + if(isBlank(cells['name_role_4'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name_role_URI_4'].value + '">' + cells['name_role_4'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['name_5'].value), '', '<name'+ if(isBlank(cells['name_URI_5'].value), '', ' valueURI="' + cells['name_URI_5'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_5'].value + '</namePart>' + if(isBlank(cells['name_role_5'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name_role_URI_5'].value + '">' + cells['name_role_5'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['name_6'].value), '', '<name'+ if(isBlank(cells['name_URI_6'].value), '', ' valueURI="' + cells['name_URI_6'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_6'].value + '</namePart>' + if(isBlank(cells['name_role_6'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name_role_URI_6'].value + '">' + cells['name_role_6'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['name_7'].value), '', '<name'+ if(isBlank(cells['name_URI_7'].value), '', ' valueURI="' + cells['name_URI_7'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_7'].value + '</namePart>' + if(isBlank(cells['name_role_7'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name_role_URI_7'].value + '">' + cells['name_role_7'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['name_8'].value), '', '<name'+ if(isBlank(cells['name_URI_8'].value), '', ' valueURI="' + cells['name_URI_8'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_8'].value + '</namePart>' + if(isBlank(cells['name_role_8'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name_role_URI_8'].value + '">' + cells['name_role_8'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['name_9'].value), '', '<name'+ if(isBlank(cells['name_URI_9'].value), '', ' valueURI="' + cells['name_URI_9'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_9'].value + '</namePart>' + if(isBlank(cells['name_role_9'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name_role_URI_9'].value + '">' + cells['name_role_9'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['name_10'].value), '', '<name'+ if(isBlank(cells['name_URI_10'].value), '', ' valueURI="' + cells['name_URI_10'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_10'].value + '</namePart>' + if(isBlank(cells['name_role_10'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name_role_URI_10'].value + '">' + cells['name_role_10'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['name_11'].value), '', '<name'+ if(isBlank(cells['name_URI_11'].value), '', ' valueURI="' + cells['name_URI_11'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_11'].value + '</namePart>' + if(isBlank(cells['name_role_11'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name_role_URI_11'].value + '">' + cells['name_role_11'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['name_12'].value), '', '<name'+ if(isBlank(cells['name_URI_12'].value), '', ' valueURI="' + cells['name_URI_12'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_12'].value + '</namePart>' + if(isBlank(cells['name_role_12'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name_role_URI_12'].value + '">' + cells['name_role_12'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['name_13'].value), '', '<name'+ if(isBlank(cells['name_URI_13'].value), '', ' valueURI="' + cells['name_URI_13'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_13'].value + '</namePart>' + if(isBlank(cells['name_role_13'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name_role_URI_13'].value + '">' + cells['name_role_13'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['name_14'].value), '', '<name'+ if(isBlank(cells['name_URI_14'].value), '', ' valueURI="' + cells['name_URI_14'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_14'].value + '</namePart>' + if(isBlank(cells['name_role_14'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name_role_URI_14'].value + '">' + cells['name_role_14'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['name_16'].value), '', '<name'+ if(isBlank(cells['name_URI_16'].value), '', ' valueURI="' + cells['name_URI_16'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_16'].value + '</namePart>' + if(isBlank(cells['name_role_16'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name_role_URI_16'].value + '">' + cells['name_role_16'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['subject_geographic'].value), '', '<subject><geographic' + if(isBlank(cells['subject_geographic_URI'].value), '>', ' valueURI="' + cells['subject_geographic_URI'].value + '">') + cells['subject_geographic'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_topic'].value), '', '<subject><topic' + if(isBlank(cells['subject_topic_URI'].value), '>', ' valueURI="' + cells['subject_topic_URI'].value + '">') + cells['subject_topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_2'].value), '', '<subject><topic' + if(isBlank(cells['subject_topic_URI_2'].value), '>', ' valueURI="' + cells['subject_topic_URI_2'].value + '">') + cells['subject_topic_2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_3'].value), '', '<subject><topic' + if(isBlank(cells['subject_topic_URI_3'].value), '>', ' valueURI="' + cells['subject_topic_URI_3'].value + '">') + cells['subject_topic_3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_navigation'].value), '', '<subject><topic' + if(isBlank(cells['navigation_URI'].value), '>', ' valueURI="' + cells['navigation_URI'].value + '">') + cells['subject_navigation'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject><name' + if(isBlank(cells['subject_name_URI'].value), '>', ' valueURI="' + cells['subject_name_URI'].value + '">') + '<namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['series_name'].value), '', '<relatedItem type="series"><titleInfo><title>' + cells['series_name'].value + '</title></titeInfo></relatedItem>}}
{{'<relatedItem type="host" displayLabel="Digital Collection"><titleInfo><title>' + cells['project_title'].value + '</title></titleInfo></relatedItem>'}}
{{'<recordInfo><recordContentSource valueURI="' + cells['source_URI'].value + '">' + cells['record_source'].value + '</recordContentSource></recordInfo>'}}
{{if(isBlank(cells['repository'].value), '', '<location><physicalLocation valueURI="' + cells['repository_URI'].value + '">' + cells['repository'].value + '</physicalLocation></location>')}}
{{'<language><languageTerm type="code" authority="iso639-2b">eng</languageTerm></language><typeOfResource>' + cells['item_type'].value + '</typeOfResource>'}}
{{'<accessCondition type="use and reproduction" xlink:href="' + cells['rights_URI'].value + '">' + cells['standardized_rights'].value + '</accessCondition>'}}
</mods>

```

## Row Separator

**LEAVE BLANK**

## Suffix

```
</modsCollection>
```