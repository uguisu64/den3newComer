<script>
    let { isSelected = false, text = "null" , onclick = () => {}} = $props()
    const className = isSelected => {if(isSelected){return "btn_design selected"}else{return "btn_design"}}
</script>


<button class={className(isSelected)} onclick={onclick}>{text}</button>

<style>
    .btn_design {
        margin-top: 10px;
        text-align: center;
        font-weight: bold;
        padding: 8px 10px;
        background-color: #e3f2fd;
        color: #000000;
        border-color:rgba(0, 0, 0, 0);
        -webkit-box-sizing: border-box;
        -moz-box-sizing: border-box;
        box-sizing: border-box;
        width: auto;
    }
  
/* マウスオーバー時 */
    .btn_design:hover{
        cursor: pointer;
        border-bottom: 3px solid #ffff00;
    }

    .selected {
        border-bottom: 3px solid #ffff00;
    }
</style>