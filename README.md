# wangEditor-farsi
ویرایشگر متن wangEditor با عناوین فارسی

```
<div id="toolbar-container"></div>
<div id="editor-container" style="border: 1px solid #ccc; min-height: 200px;"></div>
<link href="https://unpkg.com/@wangeditor/editor@latest/dist/css/style.css" rel="stylesheet">
<script src="https://unpkg.com/@wangeditor/editor@latest/dist/index.js"></script>
<script>
const { createEditor, createToolbar } = window.wangEditor
const E = window.wangEditor

E.i18nAddResources('fa', {
    // header
    header: {
        title: "ابعاد متن",
        text: "متن عادی"
        
    },
    blockQuote: {
        title: "نقل قول",
        text: "نقل قول"
    },
    textStyle: {
        bold: "پررنگ",
        italic: "خمیده",
        underline: "زیرخط",
        code: "کد",
        through: "خط خورده",
        sup: "بالا",
        sub: "پایین",
        clear: "پاک کردن سبک متن"


    },
    color: {
        color: "رنگ متن",
        default: "پیش فرض",
        bgColor: "رنگ پس زمینه",
        clear: "پاک کردن رنگ پس زمینه",
    },
    fontSize: {
        default: "پیش فرض",
        title: "اندازه فونت",
    },
    fontFamily: {
        default: "پیش فرض",
        title: "فونت",
    },
    lineHeight: {
        default: "پیش فرض",
        title: "ارتفاع خط",
    },
    listModule: {
        unOrderedList: "لیست بدون ترتیب",
        orderedList: "لیست ترتیبی",
    },
    todo: {
        todo: "چک لیست"
    },
    justify: {
        left: "چپ چین",
        center: "وسط چین",
        right: "راست چین",
        justify: "تراز شده"
    },
    indent: {
        increase: "افزایش تورفتگی",
        decrease: "کاهش تورفتگی"
    },
    emotion: {
        title: "شکلک ها"
    },
    link: {
        insert: "افزودن پیوند",
        text: "متن پیوند",
        url: "آدرس پیوند",
    },
    common: {
        ok: "تایید",
        enter: "enter",
    },
    image: {
        netImage: " تصویر اینترنتی",
        src: "آدرس تصویر",
        desc: "توضیحات تصویر",
        link : "پیوند تصویر (اختیاری)",
    },
    uploadImgModule: {
        uploadImage: "بارگذاری تصویر"
    },
    videoModule:{
        insertVideo: "افزودن ویدیو",
        videoSrc: "آدرس ویدیو",
        videoPoster: "پوستر ویدیو (اختیاری)",
        ok: "تایید",
        videoSrcPlaceholder: "آدرس ویدیو را وارد کنید",
        videoPosterPlaceholder: "آدرس پوستر ویدیو را وارد کنید (اختیاری)",
        uploadVideo: "بارگذاری ویدیو",
    },
    tableModule: {
        insertTable: "افزودن جدول",
        header: "سرصفحه",
        widthAuto: "عرض خودکار",
        insertRow: "افزودن ردیف",
        deleteRow: "حذف ردیف",
        insertCol: "افزودن ستون",
        deleteCol: "حذف ستون",
        deleteTable: "حذف جدول",
    },
    codeBlock: {
        title: "بلوک کد",
    },
    divider: {
        title: "خط جداکننده",
    },
    undo: {
        undo: "بازگشت",
        redo: "بازانجام"
    },
    fullScreen: {
        title: "تمام صفحه",
    }

    // ... other words config ...
})



E.i18nChangeLanguage('fa')






const editorConfig = {
    placeholder: 'Type here...',
    onChange(editor) {
      const html = editor.getHtml()
      console.log('editor content', html)
      // You can sync HTML to <textarea>
    },
    MENU_CONF: {}

}
editorConfig.MENU_CONF['fontFamily'] = {
    fontFamilyList: [
        {name : 'ایران سنس', value: 'iranSans'},
        'sans-serif',
        'Arial',
        'Times New Roman',
        'Impact',
        'brush-script',
        'Courier New',
    ]
}


const editor = createEditor({
    selector: '#editor-container',
    html: '<p><br></p>',
    config: editorConfig,
    mode: 'default', // or 'simple'
})

const toolbarConfig = {}

const toolbar = createToolbar({
    editor,
    selector: '#toolbar-container',
    config: toolbarConfig,
    mode: 'default', // or 'simple'
})
</script>
```
