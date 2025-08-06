# How to get JSON type images

## Example long-hand using in-line style
<span title="TAG_Byte">
    <span class="sprite nbt-sprite" style="background-position:-0px -0px;background-size:64px auto;height:16px;width:16px"></span>
</span>
<span title="TAG_Boolean">
    <span class="sprite nbt-sprite" style="background-position:-48px -32px;background-size:64px auto;height:16px;width:16px"></span>
</span>
<span title="TAG_Short">
    <span class="sprite nbt-sprite" style="background-position:-16px -16px;background-size:64px auto;height:16px;width:16px"></span>
</span>
<span title="TAG_Int">
    <span class="sprite nbt-sprite" style="background-position:-48px -0px;background-size:64px auto;height:16px;width:16px"></span>
</span>
<span title="TAG_Long">
    <span class="sprite nbt-sprite" style="background-position:-0px -16px;background-size:64px auto;height:16px;width:16px"></span>
</span>
<span title="TAG_Float">
    <span class="sprite nbt-sprite" style="background-position:-32px -0px;background-size:64px auto;height:16px;width:16px"></span>
</span>
<span title="TAG_Double">
    <span class="sprite nbt-sprite" style="background-position:-16px -0px;background-size:64px auto;height:16px;width:16px"></span>
</span>
<span title="TAG_String">
    <span class="sprite nbt-sprite" style="background-position:-32px -16px;background-size:64px auto;height:16px;width:16px"></span>
</span>
<span title="TAG_List">
    <span class="sprite nbt-sprite" style="background-position:-32px -32px;background-size:64px auto;height:16px;width:16px"></span>
</span>
<span title="TAG_Compound">
    <span class="sprite nbt-sprite" style="background-position:-48px -16px;background-size:64px auto;height:16px;width:16px"></span>
</span>
<span title="TAG_Byte_Array">
    <span class="sprite nbt-sprite" style="background-position:-0px -32px;background-size:64px auto;height:16px;width:16px"></span>
</span>
<span title="TAG_Int_Array">
    <span class="sprite nbt-sprite" style="background-position:-16px -32px;background-size:64px auto;height:16px;width:16px"></span>
</span>
<span title="TAG_Long_Array">
    <span class="sprite nbt-sprite" style="background-position:-0px -48px;background-size:64px auto;height:16px;width:16px"></span>
</span>

## Example shorthand using classes
<span title="TAG_Byte"><span class="sprite nbt-sprite tag-byte"></span></span>
<span title="TAG_Boolean"><span class="sprite nbt-sprite tag-boolean"></span></span>
<span title="TAG_Short"><span class="sprite nbt-sprite tag-short"></span></span>
<span title="TAG_Int"><span class="sprite nbt-sprite tag-int"></span></span>
<span title="TAG_Long"><span class="sprite nbt-sprite tag-long"></span></span>
<span title="TAG_Float"><span class="sprite nbt-sprite tag-float"></span></span>
<span title="TAG_Double"><span class="sprite nbt-sprite tag-double"></span></span>
<span title="TAG_String"><span class="sprite nbt-sprite tag-string"></span></span>
<span title="TAG_List"><span class="sprite nbt-sprite tag-list"></span></span>
<span title="TAG_Compound"><span class="sprite nbt-sprite tag-compound"></span></span>
<span title="TAG_Byte_Array"><span class="sprite nbt-sprite tag-byte-array"></span></span>
<span title="TAG_Int_Array"><span class="sprite nbt-sprite tag-int-array"></span></span>
<span title="TAG_Long_Array"><span class="sprite nbt-sprite tag-long-array"></span></span>

## Example Tree view
<div class="treeview">
<ul><li><span title="TAG_Compound"><span class="sprite nbt-sprite" style="background-position:-48px -16px;background-size:64px auto;height:16px;width:16px"></span></span><span class="nowrap" style="font-weight: bold;">&nbsp;tag</span>: Parent tag.</li></ul>
<ul><li><ul><li><span title="TAG_Int"><span class="sprite nbt-sprite" style="background-position:-48px -0px;background-size:64px auto;height:16px;width:16px"></span></span><span class="nowrap" style="font-weight: bold;">&nbsp;Damage</span>: The number of uses <i>consumed</i> (not remaining) of the item's <a href="/wiki/Durability" title="Durability">durability</a>.</li>
<li><span title="TAG_Byte"><span class="sprite nbt-sprite" style="background-position:-0px -0px;background-size:64px auto;height:16px;width:16px"></span></span><span class="nowrap" style="font-weight: bold;">&nbsp;Unbreakable</span>: 1 or 0 (true/false) - if true, the item doesn't lose durability when used.</li>
<li><span title="TAG_List"><span class="sprite nbt-sprite" style="background-position:-32px -32px;background-size:64px auto;height:16px;width:16px"></span></span><span class="nowrap" style="font-weight: bold;">&nbsp;CanDestroy</span>: The only blocks this item may break when used by a player in <a href="/wiki/Adventure" title="Adventure">adventure mode</a>.
<ul><li><span title="TAG_String"><span class="sprite nbt-sprite" style="background-position:-32px -16px;background-size:64px auto;height:16px;width:16px"></span></span>: A block ID. Validated the same way as the <a href="/wiki/Argument_types#block_predicate" title="Argument types"><code>block_predicate</code> command argument</a>, meaning block states and block tags are accepted, as well as <b>client-side only</b> block entity NBT tags.</li></ul></li>
<li><span title="TAG_Int"><span class="sprite nbt-sprite" style="background-position:-48px -0px;background-size:64px auto;height:16px;width:16px"></span></span><span class="nowrap" style="font-weight: bold;">&nbsp;CustomModelData</span>: A value used in the <code>"custom_model_data"</code> <a href="/wiki/Model#Item_tags" title="Model">item tag</a> in the overrides of item models.</li></ul></li></ul>
</div>


### Types

- TAG_Byte
- TAG_Boolean
- TAG_Short
- TAG_Int
- TAG_Long
- TAG_Float
- TAG_Double
- TAG_String
- TAG_List
- TAG_Compound
- TAG_Byte_Array
- TAG_Int_Array
- TAG_Long_Array

