smartformsAPI

1�����ܱ�ƽ̨API�ӿڣ� 2������ҵ��ƽ̨API�ӿڣ�
��չʹ��˵��

1��Ŀ¼˵�� com.gzsolartech.smartforms. --api --controller ���Ʋ� --mode DTO�� --service ҵ���߼����ݴ����

--entity ʵ����

2����չʹ�� (1) �ڿ��Ʋ㴴��controller�࣬�̳�BaseApiController (2) ��controller����ͷ�����

    @Controller    // ע����Ʋ��ʶ
    @RequestMapping("/api/datAppAcl")   //ӳ�����·��
    @Api(tags="Application library permissionsl")  //��ӶԸ�api ���Ʋ��˵��

(3) ��controller����ͷ�����

	@ApiOperation(notes = "��ȡӦ�ÿ��aclȨ��",  httpMethod = "POST", value = "��ȡӦ�ÿ��aclȨ��")  //��ӷ���ע��˵��
@RequestMapping(value="/getAllAppAcl",method=RequestMethod.POST)   //ӳ�����·��    ��������ʽGET��POST��DELETE��PUT
@ResponseBody    

(4) ���controller��������˵�������²���

// 	required�Ƿ���������nameֵ��Ӧ�������ԣ�value Ϊ����˵��   @RequestParam ����Ϊ��������
	@ApiParam(required = true, name = "token", value = "�û���ʶ����")  @RequestParam String token    
